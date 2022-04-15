# Rogue snapshotting using CRIU

Rogue is a difficult, random game. And if you die, that's it, game over. 

You can't save your game in Rogue, so your hours are just lost.†

![rogue game over screen](img/dead_screen.png)

But - if you can suspend the running process into files using CRIU, that gives you a save feature. 

Let's make our own savegame feature by snapshotting the whole process! 

This repo demonstrates using [CRIU](https://criu.org/Main_Page) to snapshot Rogue.

## Usage

### Running

Build it: `docker build -t criu-rogue .`

Run it: `docker run -v $PWD/saves:/saves --privileged -it criu-rogue`

Play it: `tmux`, then `rogue`

### Saving

We'll be snapshotting the whole tmux session.

CRIU can't snapshot it while you're attached. So detach with `Ctrl+b, d` first. 
(Ctrl+b enters the tmux Command Mode, and "d" detaches.)

Run `save save1`. This will snapshot the tmux process tree to the `/saves/save1` dir.

### Loading

Run `load save1`. It will load the tmux process tree from disk.

Make sure you're not already running tmux, of course.
(Quit Rogue with `Shift+Q, y` if needed. `exit` to quit tmux.)

Then attach to the tmux session with `tmux attach`.

## Notes

### Ideas






Export the container: `docker export ro-1 > ro-1.tgz` 

Resume the original: `docker start ro-1; docker attach ro-1`

Load exported container as a new image: `cat ro-1.tgz | docker import - ro-1-img`

Run the new image: `docker run -t -i --privileged --name ro-2 ro-1-img wrapper`

Now you have:

```
> docker ps

CONTAINER ID   IMAGE        COMMAND     CREATED          STATUS          PORTS     NAMES
719d4d975640   ro-1-img     "wrapper"   6 seconds ago    Up 4 seconds              ro-2
57fa293e8daf   criu-rogue   "wrapper"   55 seconds ago   Up 20 seconds             ro-1
```

And you've got two Rogues:
![two copies of the same rogue game](img/double-rogue.png)

## How it works

Original implementation is from the [critmux](https://github.com/jpetazzo/critmux) repo.

After stopping / starting the container, the `/state` directory is still there. If you like, you can copy its contents out as well, via `docker cp ro-1:/state .` The state dir is small (1.7 MB) - a nice alternative to creating 500MB dockers just to save and load your Rogue game. You would need to adjust the container's `wrapper` script to point at a different dir in order to load your saved state back in. A good improvement idea.

## Notes

This method can be applied to any process, of course. Rogue / Nethack types of games are just a nice example use case. Since this method lets you save at any instant in a game, it could be great for tool-assisted speedrunning, debugging, or game-playing AI development.

Since rogue is running in tmux, Ctrl+b will do tmux things rather than moving down-left fast.

† Some versions of Rogue later added a save feature, but the typical Rogue on Ubuntu / Debian doesn't have one. Instead it has a sort of pause feature. You can "save", but the save file is deleted when you load it. There's also protection against copying the file: it checks if the inode has changed. This is not easy to circumvent. You'd have to change the source code, hex-edit the save file, or do some low-level hacking on your filesystem. Snapshotting is nicer; it'll work on this, and on many other problems too.

If you haven't played Rogue before, start with the [manual](docs/rogue-manual.pdf). To learn strategies, consult the [tables](docs/tables.md) and [tips](docs/tips.md) pages. Or consult the [source code](https://salsa.debian.org/ucko/bsdgames-nonfree/-/tree/master).

![rogue win screen](img/win.png)

Happy savescumming!



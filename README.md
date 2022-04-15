# Rogue save states using CRIU

Rogue is a difficult, random game. And if you die, that's it, game over. 

You can't save your game in Rogue, so your hours are just lost.†

![rogue game over screen](img/dead_screen.png)

But using CRIU, we can dump running processes to disk and load them back.

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

### Portability

Each save is a few megabytes. They will show up in the `saves/` subdirectory outside the container.

A save game created in one container should be usable in another container launched from the same OS.
It is not known how kernel-dependent the saves are.

## Notes

### Beyond Rogue

![ninvaders](img/ninvaders.png)

The criu-rogue docker actually works on *anything* you can run in tmux. For more games, just do `apt-get install ninvaders` or `nethack-consolegames` to try those. Save and load is the same process.

Since you can save-state at any instant, it could be great for tool-assisted speedrunning, debugging, or AI development. 

Of course, it won't work on network-connected applications; you'd have to snapshot the Internet along with it.

### More CRIU

CRIU is a powerful and underused tool. It's not just for games! Caching the state of a whole application could skip many computations. Further, you don't need to modify the source code to use CRIU, or even have it. 

See also:

 [Critmux](https://github.com/jpetazzo/critmux) inspired this project. It connects CRIU's suspend / resume functions to Docker's start and stop features. 
 
 [Docker Checkpoint](https://docs.docker.com/engine/reference/commandline/checkpoint/) is also a thing.

### About Rogue

† Some versions of Rogue later added a save feature, but the typical Rogue on Ubuntu / Debian doesn't have one. Instead it has a sort of pause feature. You can "save", but the save file is deleted when you load it. There's also protection against copying the file: it checks if the inode has changed. This is not easy to circumvent. You'd have to change the source code, hex-edit the save file, or do some low-level hacking on your filesystem. Snapshotting is nicer; it'll work on this, and on many other problems too.

If you haven't played Rogue before, start with the [manual](docs/rogue-manual.pdf). To learn strategies, consult the [tables](docs/tables.md) and [tips](docs/tips.md) pages. Or consult the [source code](https://salsa.debian.org/ucko/bsdgames-nonfree/-/tree/master) itself.


![rogue win screen](img/win.png)

Best of luck on your journey to the Amulet and back.
# project-ideas
A list of project ideas I'm too dumb or incompetent to work on myself, feel free to take them and create your own projects.

## Intro
I often come up with project ideas that would be great to use, but would never be able to work on.
To stop me from working on these oneshot projects I decided to put these out for the ones who do want to work on them.

These ideas are free for anyone to work on.
You are free to use them however you like, but I like to propose 2 guidelines:

1. Proper credit is given.
2. The project is open-source.

These rules don't need to be followed, but I consider them rational and friendly.

The reason is that this allows everyone to benefit from the software inspired here.

---

## Project list
### Index

- [Auto-DJ](#Auto-DJ)
- [Client-Server Text Editor](#Client-Server-Text-Editor)

### Auto-DJ
Difficulty: Hard

A program that can assist Dj's by giving them approprate song suggestion based on the current song playing and times transitions to other songs.
The idea is to take away a lot of the gruntwork and human-error-prone phases of Dj's allowing them to spend time on other tasks.
Ideally there should also be an autoplay mode for at-home consumption.

### Client-Server Text Editor
Difficulty: Very hard

An extensible text editor with proper client-server architecture.
While you could hack this functionality into vim or use emacs, this text editor is supposed to be a more refined implementation of client-server text editing.

In this model there are two (possibly more depending on implementation and scale) roles that need to be fullfilled.

Server:
- Read Write and manage files
- Present those files to 1 or more clients (either locally or over a network connection)
- Allow clients to modify these files with different permissions based on who owns the file
- Allow more than 1 client to edit a file at the same time (with real time preview)
- Allow for server plugins

Client:
- Start a local server when editing locally or connect with a running server
- Give signal to a remote service to edit a file
- Connect to local and remote servers and send changes
- be able to communicate with other clients to send peer-to-peer data (Suggestion)
- Allow for client plugins

The bast way of handling client requests is to set up a service separate from the ones handling the files.
Ideally only the protocol should be standardized to allow for different servers and clients to communicate.

# Files and Serialization

## Learning Outcomes

- What are two ways to store a file from your hard drive into a string or array in your Ruby script?
- What are three things made possible or much easier by serialization?
- What is JSON?
- What is YAML?
- How do you turn a Ruby object into JSON?
- How do you turn JSON into a Ruby object?

## IO Class

Ruby has the input/output class (IO) which contains standard input (stdin), standard output (stdout) and standard error (stderr)

### Files

A Ruby File object is a subclass of IO, and the most well known.

### Sockets

- TCP Socket
  - Represents a TCP/IP client socket
- UDP Socket
  - Represents a UDP/IP socket. (User Datagram Protocol) - Especially time-sensitive transmissions such as video playback or DNS lookups.
- UNIX Socket
  - Represents a UNIX domain stream client socket.
- Socket
  - Provides access to underlying operating system socket implementations. It can be used to provide more operating system specific functionality than the protocol-specific socket classes.

### StringIO

Allows strings to behave like IOs. Able to use strings into systems that consume streams.

This one does not actually inherit from IO class but is it's own thing.

### Tempfile

Similar to StringIO, does not inherit from IO. It implements File's interface and deals with temporary files.

It can be passed to any object taht consumes IO-like objects, so I guess it can be considered a duck type.

# Files and Serialization

Serialization is taking complex data structures and "flattening" them into a string that can be sent to other users/machines and reconstructed.

## Learning Outcomes

- What are two ways to store a file from your hard drive into a string or array in your Ruby script?
-
- What are three things made possible or much easier by serialization?
  - Transferring large amounts of data, quickly writing scripts to files, quickly reading information from a file, sending objects/data structures.
- What is JSON?
  - Javascript Object Notation. A common serialization format. All elements are comma separated, arrays by brackets, objects by curly braces.
- What is YAML?
  - Another serialization format/notation where the number of spaces determine the level of nesting.
  - This format allows it to be more easily read by humans. Used in Rails
  - Stands for YAML Ain't Markup Language
- How do you turn a Ruby object into JSON?
  - Using the JSON ruby module.
- How do you turn JSON into a Ruby object?
  - Using the JSON ruby module.

## Learning Questions

- How would you go through the lines of a file using the IO object in the command line?
-
- How would you take the Array [1,2,3] and serialize it into a JSON string format?
-
- What are the benefits of YAML vs JSON vs MessagePack serialization formats?
  - YAML is very human readable, JSON is written in Javascript so it's built for the web and also human readable and almost identical format to Ruby hash format, MessagePack is built for speed.
- How would you check if a file exists using the File object in the command line?
-
- In a Download directory containing 5 files, how would you count the number of files in that directory using the Dir object?

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

It can be passed to any object that consumes IO-like objects, so I guess it can be considered a duck type.

## File Input/Output

#### Creating a file and writing to it

```Ruby
somefile = File.open(filename, "W")
somefile.puts "Writing this to the file"
somefile.close
```

WARNING: "w" will erase the current contents of the file, use append, "a" if you want to add to the end of the file.

#### Reading from a File

```Ruby
file = File.open("sample.txt", "r")
contents = file.read
puts contents
```

Keep in mind calling read again on file would try to continue reading from where it left off (the end of the file)

# JAVA
What is JAVA: 
- Programming Language
- Runtime Environment (JRE/ Java SE)

JavaFX:
- to create rich client application
- a library of classes
- call JRE into JavaFX classes

# STREAM
- an ordered sequence of data
- Provides a common I/O model
- Abstracts details
- Stream types are unidirectional (either read from or write to)

Types of STREAM: -
1. Byte streams 
    - interact as binary data 
    - i.e. 01101110
    - `InputStream` & `OutputStream` classes
2. Text streams
    - interact as Unicode characters
    - `Reader` & `Writer` classes

## Stream classes
### Byte streams
#### InputStream
1. ByteArrayInputStream: Allowed to create a stream over a `byte array `(Create managed memory -> a way to use streams)
2. PipedInputStream: 
    - Producer-consumer relationship
    - To `read` content back out (For different part of program). 
3. FileInputStream: Allowed to create a stream over `files`.

#### OutputStream
1. ByteArrayOutputStream: Allowed to create a stream over a `byte array` (Create managed memory -> a way to use streams)
2. PipedOutputStream:  
    - Producer-consumer relationship
    - To `write` content into it (for 1 part of program). 
3. FileOutputStream: Allowed to create a stream over `files`.

### Text streams
#### Reader
1. CharArrayReader: Allowed to create an `character array` -> put stream over top of them. 
2. StringReader: Allowed to work with `string buffer`.
3. PipedReader:
    - Producer-consumer relationship
    - To `consume` content
4. InputStreamReader:
    - Create a reader over an input stream.
    - get `input stream` (Binary stream) -> put `InputStreamReader`
    - To consume it as `text stream` (layering stream together)
    - FileReader:
        - Inherit class
        - Allowed to have `file-based` content with reader
#### Writer
1. CharArrayWrite: Allowed to create an `character array` -> put stream over top of them. 
2. StringWriter: Allowed to work with `string buffer`.
3. PipedWriter:
    - Producer-consumer relationship
    - To `produce` content.
4. OutputStreamWriter:
    - Create a writer over an output stream.
    - get `output stream` (Binary stream) -> put `OutputStreamWriter`
    - To produce it as `text stream` (layering stream together)
    - FileWriter:
        - Inherit class
        - Allowed to have `file-based` content with writer

## Error Handling & Cleanup
Error handling
- Indicate errors: Throw exceptions.
Cleanup
- Not rely on standard Java resource recovery to clean up streams.
- Reason: Streams backed by physical storage (often exist `outside` i.e. files, network connections)


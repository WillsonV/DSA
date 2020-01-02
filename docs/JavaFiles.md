## How to Download a File from a URL in Java.

## Using Java NIO

Java NIO is an alternative package to handle networking and input-output operations in Java. The main advantage that the Java NIO package offers is that it's non-blocking, and has channeling and buffering capabilities. When we use the Java IO library we work with streams that read data byte by byte. However, the Java NIO package uses channels and buffers. The buffering and channeling capabilities allow the system to copy contents from a URL directly into the intended file without needing to save the bytes in application memory, which would be an intermediary step. The ability to work with channels boosts performance.

In order to download the contents of a URL, we will use the ReadableByteChannel and the FileChannel classes.

     ReadableByteChannel readChannel = Channels.newChannel(new URL("http://example.com/my-file-path.txt").openStream());
     
The ReadableByteChannel class creates a stream to read content from the URL. The downloaded contents will be transferred to a file on the local system via the corresponding file channel.
     
         FileOutputStream fileOS = new FileOutputStream("/Users/username/Documents/file_name.txt");
FileChannel writeChannel = fileOS.getChannel();

After defining the file channel we will use the transferFrom() method to copy the contents read from the readChannel object to the file destination using the writeChannel object.

    writeChannel.transferFrom(readChannel, 0, Long.MAX_VALUE);
  
  The transferFrom() and transferTo() methods are much more efficient than working with streams using a buffer. The transfer methods enable us to directly copy the contents of the file system cache to the file on the system. Thus direct channeling restricts the number of context switches required and enhances the overall code performance.

Now, in the following sections, we will be looking at ways to download files from a URL using third-party libraries instead of core Java functionality components.

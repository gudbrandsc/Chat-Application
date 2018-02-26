## What is Chat app?
Chat app is an application that was part of my university course in Distributed Software Development. The application let's users send and receive both private and broadcast messages in the zookeeper cluster. It also include a UDP client and server to support reliable bulk download of the History data structure of another chat peer in the network.

This chat application is implemented using the following technologies.
- Sockets
- ZooKeeper
- Protocol Buffers
- UDP Sockets

## Application Interface 

1. **List** - all other chat nodes in the network.
2. **Send a message** - to a specific node.
3. **Broadcast** - Send a message to all other nodes.
4. **Receive and display** - a message from another node.
5. **Show history** - The user must be able to display the contents of its current history data structure.
6. **Download history** - The user may request to download the entire broadcast chat history from another peer.
7. **Help** - list the commands available to the user.
8. **Exit** - application

## Application Execution

- The program takes three command line arguments:
  * `-user <username>` - The username that will be used for your client.
  * `-port <port>` - The port on which your server will listen.
  * `-udpport <port>` - The UDP port on which your download service will listen.

The program *must* run exactly as follows, where name, 9900, and 9901 will be replaced with appropriate values:
```
java -cp project2.jar cs682.Chat -user name -port 9900 -udpport 9901


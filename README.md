# Server_Client

This project will allow for a creation of a server capable of managing the communication between several clients.

-----------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------

**How to compile**

Is possible to compile by hand:

$ gcc Server.c -o server.elf -lpthread
$ gcc Client.c -o client.elf -lpthread -lrt

------

Or this can also be made using the make file by the following commands:

	$ make server
	$ make client

Using 'make clear' will remove any .o or .elf files from the directory.
It's also possible to compile to the Raspberry Pi 4, see makefile documentation for more on that.

-----------------------------------------------------------------------------------------------------

**How to start**

*PORT* -> socket that serves as a connector between the server and the clients (ex.: 5000)
*IP* -> IP address of the client (ex.: 127.0.0.1)

Initizale the server: 
	$ ./server.elf <PORT>

Initialize a client: 
	$ ./client.elf  <IP> <PORT>
	$ <name>

------

**How to use**

On the client window it will appear an '>' when the client is able to send a message. To do that the client just needs to type the message and press ENTER to send it.
When a client receives a message it will appear in its screen in the format '> <sender> -> <message>'.
When the server sends a notification to a client it appears in the format '<clientName>: <notification>.
To leave the server a client needs to type 'exit' and press ENTER. A 'Bye' message will appear and the program terminates on the client side.

The server program only terminates when there's no more clients left. 


-----------------------------------------------------------------------------------------------------


**Current features**

-> *Multiple clients allowed*.

-> *Messagign between different clients*: After a name as been given we can send a message to all the other clients and receive as well.

-> *AFK state*: If we spend more than 1 minute without sending a message the server will attribute an AFK state. Every 5seconds the server checks every client's state. 

-> *Client's actions notifications*: If a client joins or leaves a message is sent to all the remaing clients by the server notifying them of that action.


-----------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------


**Next step is:**

	->  create a ./sendout <message>
	-> using a device driver turn on the green led when there's a new message and turn it off when a message is sent
	-> make the AFK state change in the client and not by the server (SIGNALS maybe?)
	-> create private channels with specific clients
		



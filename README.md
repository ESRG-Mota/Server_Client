# Server_Client

-----------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------

**How to start**

Initizale the server: 
$ ./server.elf <PORT>

Initialize a client: 
$ ./client.elf  <IP> <PORT>
$ <name>

-----------------------------------------------------------------------------------------------------

**Current features**

After a name as been given we can send a message to all the other clients and receive as well.
If we spend more than 1 minute without sending a message the server will attribute an AFK state. Every 5seconds the server checks every client's state. 
If a client joins or leaves a message is sent to all the remaing clients by the server notifying them of that action.

-----------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------

**Next step is:**

	->  create a ./sendout <message>
	-> using a device driver turn on the green led when there's a new message and turn it off when a message is sent
	-> make the AFK state change in the client and not by the server (SIGNALS maybe?)
	-> create private channels with specific clients
		



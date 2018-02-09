Intern_task
/*The file can be run directy in the PC with installed python. In order to run the file, I request you to run file server.py initially in a terminal and client.py in another terminal.
Now can start sending messages from Client terminal to Server terminal and back. This communication set-up is using basic socket programming in Python. */ 

Here is the summary of the key functions from socket - Low-level networking interface:

socket.socket(): Create a new socket using the given address family, socket type and protocol number.

socket.bind(address): Bind the socket to address.

socket.listen(backlog): Listen for connections made to the socket. The backlog argument specifies the maximum number of queued connections and should be at least 0;

socket.accept(): The return value is a pair (conn, address) where conn is a new socket object usable to send and receive data on the connection, and address is the address bound to the socket on the other end of the connection.

At accept(), a new socket is created that is distinct from the named socket. This new socket is used solely for communication with this particular client.


Limitations of the server code: The server code above can only interact with one client.in order to connect with a second terminal it simply won’t reply to the new client. To let the server interact with multiple clients, need to use multi-threading and rebuild the server script to accept multiple client connections:

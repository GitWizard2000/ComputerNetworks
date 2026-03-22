# TCP Client-Server in C

This project demonstrates a simple TCP client-server communication in C using sockets. The server listens for incoming connections and responds to messages from the client.

## Files
- `server.c`: TCP server implementation
- `client.c`: TCP client implementation

## How It Works
- The server listens on IP `127.0.0.1` and port `5566`.
- The client connects to the server at the same IP and port.
- The client sends a message to the server.
- The server receives the message, prints it, and sends a response back to the client.
- The client receives and prints the server's response.

## Compilation
Use `gcc` to compile both server and client:

```
gcc server.c -o server
gcc client.c -o client
```

## Usage
1. **Start the server** (in one terminal):
   ```
   ./server
   ```
   You should see:
   ```
   [+]TCP server socket created.
   [+]Bind to the port number: 5566
   Listening...
   ```

2. **Start the client** (in another terminal):
   ```
   ./client
   ```
   You should see output like:
   ```
   [+]TCP server socket created.
   Connected to the server.
   Client: HELLO, THIS IS CLIENT.
   Server: HI, THIS IS SERVER. HAVE A NICE DAY!!!
   Disconnected from the server.
   ```

3. **Server output** will show:
   ```
   [+]Client connected.
   Client: HELLO, THIS IS CLIENT.
   Server: HI, THIS IS SERVER. HAVE A NICE DAY!!!
   [+]Client disconnected.
   ```

## Notes
- Both server and client are hardcoded to use `127.0.0.1:5566`.
- The server can handle one client at a time in a loop.
- Modify the code to change IP or port as needed.

## Requirements
- GCC compiler
- Linux or Unix-like OS

## License
This project is for educational purposes.

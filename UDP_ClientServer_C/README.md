# UDP Client-Server in C

This project demonstrates a simple UDP client-server communication using C. Both client and server run locally and exchange messages over UDP.

## Structure

- `UDP_ClientServer_C/client.c`: UDP client implementation
- `UDP_ClientServer_C/server.c`: UDP server implementation

## How It Works

- The server listens for incoming UDP messages on a specified port.
- The client sends a message to the server and waits for a response.
- The server receives the message, prints it, and sends a reply.
- The client receives the reply and prints it.

## Usage

### 1. Compile

Navigate to the `UDP_ClientServer_C` directory and compile both files:

```
gcc server.c -o server
gcc client.c -o client
```

### 2. Run Server

Start the server with a port number (e.g., 8080):

```
./server 8080
```

### 3. Run Client

In a new terminal, run the client with the same port number:

```
./client 8080
```

## Example Output

**Server:**
```
[+]Data recv: Hello, World!
[+]Data send: Welcome to the UDP Server.
```

**Client:**
```
[+]Data send: Hello, World!
[+]Data recv: Welcome to the UDP Server.
```

## Notes

- Both client and server use `127.0.0.1` (localhost).
- Change the IP address in the code if you want to run on different machines.
- The buffer size is 1024 bytes.

## Requirements

- GCC compiler
- Linux environment

## License

MIT License

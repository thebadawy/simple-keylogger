***A simple keylogger with the ability to exfiltrate key logs from the client's device to the server's device using sockets.***
_________

**Server-side script**

- Creates a socket, then binds the host and port.
- Listens for only one connection, as multi-threading is not applied.
- Opens or creates a file and appends the exfiltrated keylogs to the file.


**Client-side script**

- Creates a socket, then connects to the host IP address and port.
- Uses a keyboard listener from the Pynput library.
- Sends each keystroke to the server-side device.
- Each keystroke is encoded into a bytes object for data exfiltration using sockets.

This project implements a secure group chat application using socket programming, leveraging both UDP and TCP protocols. The application enables users to establish a connection with the server, where they exchange keys for secure communication.

Upon connecting, the server and the user perform a key exchange to generate a private key for their session. Additionally, the server provides the user with a separate group key, which is used to encrypt messages within the group chat.

In this setup:

Unicast is used for communication between the user and the server, where the user's messages are securely sent to the server.
Multicast is utilized for broadcasting messages to all group members, ensuring that each participant receives the encrypted message.
The encryption process includes:

  1.  The user encrypts their message using the shared private key before sending it to the server.
  2.  The server decrypts the message using the same shared key.
  3.  The server then re-encrypts the message using the group key and broadcasts it to all group members via multicast.
     
This approach ensures end-to-end security for both individual and group communications.

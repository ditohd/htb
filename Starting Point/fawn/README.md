# Write Up Starting Point

## Challenge - fawn

### Tentang Challenge

- Introduction

  Mempelajari sistem FTP(File Transfer Protocol) dan mekanisme standar FTP.
  berikut menurut wikipedia :

  ```
  The File Transfer Protocol (FTP) is a standard communication protocol used to transfercomputer files from a server to a client on a computer network. FTP is built on aclient–server model architecture using separate control and data connections betweenthe client and the server. FTP users may authenticate themselves with a clear-textsign-in protocol, generally in the form of a username and password. However, they canconnect anonymously if the server is configured to allow it. For secure transmissionthat protects the username and password and encrypts the content, FTP is often securedwith SSL/TLS (FTPS) or replaced with SSH File Transfer Protocol (SFTP).
  ```

  untuk mengetahui lebih lanjut bagaimana FTP bekerja silahkan lihat Write Ups <br> **[Fawn.pdf](Fawn.pdf)**

1. Task One

   > What does the 3-letter acronym FTP stand for?

   > Answer : `File Transfer Protocol`

2. Task Two

   > What communication model does FTP use, architecturally speaking?

   > Answer : `Client-Server model`

3. Task Three

   > What is the name of one popular GUI FTP program?

   > Answer : `FileZilla`

4. Task Four

   > Which port is the FTP service active on usually?

   > Answer : `21 TCP`

5. Task Five

   > What acronym is used for the secure version of FTP?

   > Answer : `SFTP`

6. Task Six

   > What is the command we can use to test our connection to the target?

   > Answer : `ping`

7. Task Seven

   > From your scans, what version is FTP running on the target?

   > Answer : `vsftpd 3.0.3`

8. Task Eight

   > From your scans, what OS type is running on the target?

   > Answer : `Unix`

9. Submit Flag

   > Submit root flag

   > Answer : `HTB{035db21c881520061c53e0536e44f815}`

### Proof Of Concept :

- Enumeration
  - Ping Target.
    <br> `Yaa kalau target down ya percuma...`
    ![ping](../../assets/Screenshot%20from%202021-12-05%2023-27-31.png)
  - Scan Open Port Using nmap
    <br> `port ftp itu default nya 21`
    <br> [Nmap Scanner](/nmap)
- Foothold
  - Login into FTP port
    <br> `Login menggunakan port default, username dan password menggunakan anonymous Authorization`
    ![login](../../assets/Screenshot%20from%202021-12-05%2023-38-25.png)

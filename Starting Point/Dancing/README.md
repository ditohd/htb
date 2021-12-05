# Write Up Starting Point

## Challenge - dancing

### Tentang Challenge

- Introduction

  Mempelajari basic dasar protocols SMB(Server Message Block). SMB berkerja di Windows.

1. Task One

   > What does the 3-letter acronym SMB stand for?

   > Answer : `Server Message Block`

2. Task Two

   > What port does SMB use to operate at?

   > Answer : `445`

3. Task Three

   > What network communication model does SMB use, architecturally speaking?

   > Answer : `client-server model`

4. Task Four

   > What is the service name for port 445 that came up in our [nmap scan](./nmap)?

   > Answer : `microsoft-ds`

5. Task Five

   > What is the tool we use to connect to SMB shares from our Linux distribution?

   > Answer : `smbclient`

6. Task Six

   > What is the `flag` or `switch` we can use with the SMB tool to `list` the contents of the share?

   > Answer : `-L`

7. Task Seven

   > What is the name of the share we are able to access in the end?

   > Answer : `WorkShares`

8. Task Eight

   > What is the command we can use within the SMB shell to download the files we find?

   > Answer : `get`

9. Submit Flag

   > Submit root flag

   > Answer : `HTB{5f61c10dffbc77a704d76016a22f1664}`

### Proof Of Concept :

- Enumeration
  - scan port target menggunakan command [`sudo nmap -sV -sC -oA nmap/dancing (IP)`](./nmap)
  - scan list Sharename Target menggunakan command `smbclient -L (IP)` dengan Guest Authentication (Leave Password Field Blank)
    ![smbclient](../../assets/Screenshot%20from%202021-12-06%2000-24-54.png)
- Foothold
  - login ke target menggunakan command `smbclient \\\\{target_IP}\\WorkShares`
  - check semua directory
    ![dir](../../assets/Screenshot%20from%202021-12-06%2000-31-15.png)
  - Dapet Flag.txt

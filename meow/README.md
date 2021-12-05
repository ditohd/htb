# Write Up Starting Point

## Challenge - Meow

### Tentang Challenge

Memahami tentang `enumeration`, dan mempelajari basic dasar dari sebuah fondasi website.

1. Task One

   > What does the acronym VM stand for?

   > Answer : `Virtual Machine`

2. Task Two

   > What tool do we use to interact with the operating system in order to start our VPN connection?

   > Answer : `Terminal`

3. Task Three

   > What service do we use to form our VPN connection?

   > Answer : `openvpn`

4. Task Four

   > What is the abreviated name for a tunnel interface in the output of your VPN boot-up sequence output?

   > Answer : `tun`

5. Task Five

   > What tool do we use to test our connection to the target?

   > Answer : `ping`

6. Task Six

   > What is the name of the script we use to scan the target's ports?

   > Answer : `nmap`

7. Task Seven

   > What service do we identify on port 23/tcp during our scans?

   > Answer : `telnet`

8. Task Eight

   > What username ultimately works with the remote management login prompt for the target?

   > Answer : `root`

9. Submit Flag

   > Submit root flag

   > Answer : `HTB{b40abdfe23665f766f9c61ecba8a4c19}`

### Proof Of Concept :

- Scan Target With nmap
- Entering Target Shell with `telnet` command
- Escape Character `^]` or `Shift + ]`
- default Login Authorization `root`
  ![telnet](https://i.ibb.co/3CpN4F4/Screenshot-from-2021-12-05-21-22-43.png)
- Root Authentication Success

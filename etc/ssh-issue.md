# SSH ISSUE

## CASE 01

### Issue

> IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY! Someone could be eavesdropping on you right now (man-in-the-middle attack)! It is also possible that a host key has just been changed. The fingerprint for the ECDSA key sent by the remote host is SHA256:bGyCow3w/n/JcSq0m82O0eKotb8lDsb+r594rtlecBo. Please contact your system administrator. Add correct host key in /Users/kkwan/.ssh/known_hosts to get rid of this message. Offending ECDSA key in /Users/kkwan/.ssh/known_hosts:17 ECDSA host key for 20.200.234.31 has changed and you have requestaed strict checking. Host key verification failed.

### Solution

```sh
ssh-keygen -R [IP or domain]
```

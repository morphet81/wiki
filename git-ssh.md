# Accessing Bitbucket or Github though SSH

1. Create you key

```bash
ssh-keygen -t rsa -C "myemail@mydomain.com" -b 4096 -f ~/.ssh/mykey
```

2. Add this key to identity
```bash
ssh-add ~/.ssh/mykey
```

3. Copy your public key
```bash
cat ~/.ssh/mykey.pub | pbcopy
```

4. Paste the key in the settings of either Github or Biibucket
* **Bitbucket**: Bitbucket Settings -> SSH Keys -> Add key
* **Github**: Settings -> SSH and GPG keys -> New SSH key
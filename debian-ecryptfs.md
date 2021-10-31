# ecryptfs on debian

Ideally I'd switch to ext4 FS encryption, but due to its weird file-moving
semantics it breaks certain daemons such as CUPS.

## Set-up

```shell
apt-get install ecryptfs-utils
ecrypt-migrate-home -u username
```

## Configure SSH (for key-based login)

Create file `/etc/ssh/sshd_config.d/ecryptfs.conf` with the following contents:

```ssh-config
AuthorizedKeysFile    .ssh/authorized_keys .ssh/authorized_keys2 /etc/ssh/authorized_keys/%u
AuthenticationMethods publickey,password
```

Now make the directory and an `authorized_keys` file for each user:

```shell
mkdir /etc/ssh/authorized_keys
chmod 0755 /etc/ssh/authorized_keys

touch /etc/ssh/authorized_keys/username
chown username: /etc/ssh/authorized_keys/username
chmod 0644 /etc/ssh/authorized_keys/username
```

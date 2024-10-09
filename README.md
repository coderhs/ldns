
# LDNS (Local DNS)

LDNS is a simple yet powerful shell script designed to streamline server management by eliminating the need to manually look up IP addresses for servers without public DNS configurations. If you've ever found yourself frustrated with managing server connections by IP addresses alone, LDNS provides an efficient solution by allowing you to easily add or remove entries in your system's hosts file.

With LDNS, you can reference a server's IP address using a hostname on your local machine.

## Key Features:
- Add or remove hostnames for quick local reference.
- Simplify SSH or other network connections by using hostnames instead of IP addresses.
  
For example, running the following command:

```bash
sudo ldns add richclient.server 42.x.x.x
```

will enable you to replace:

```bash
ssh user@42.x.x.x
```

with:

```bash
ssh user@richclient.server
```

## Usage

### Add a Host
To add a hostname to your system's hosts file, use the following command:

```bash
sudo ldns add <hostname> <IP>
```

Example:

```bash
sudo ldns add richclient.server 42.x.x.x
```

### Remove a Host
To remove a previously added hostname from the hosts file, run:

```bash
sudo ldns delete <hostname>
```

Example:

```bash
sudo ldns delete richclient.server
```

### List

List all the hostname in `/etc/hosts`

```sh
sudo ldns list
```


---

LDNS is a simple but effective tool that saves you time and effort when managing server connections locally.

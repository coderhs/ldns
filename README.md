# LDNS (Local DNS)

Ever wanted to stop looking IPs of the server you are managing? ldns is a simple shell script that was created
out of the frustration of having to manage servers with no public DNS configured. This simple program will you to add/remove
entry from the hosts file.

`sudo ldns add <hostname> <IP>` allows you to reference the ip as <hostname> in your local machine.

Doing `sudo ldns add richclient.server 42.x.x.x` would make `ssh user@42.x.x.x` to `ssh user@42.x.x.x`

## Usage

### Add

You can add an ip to hosts file using the following command
`sudo ldns add <hostname> <IP>`

```sh
sudo ldns add richclient.server 42.x.x.x
```

### Remove

To delete an entry

`sudo ldns delete <hostname>`

```sh
sudo ldns delete richclient.server
```

## How does it work?

We add an entry to the hosts file in your local machine. This is the reason why we need sudo permission as well.

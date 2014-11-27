motd
====

This role creates the Message Of The Day (motd) file with some additional
information about the distro and the hardware.


Example
-------

```
# This is a playlist example
- host: myhost
  # Load the role to produce the /etc/motd file
  roles:
    - motd
```

This playbook produces the `/etc/motd' file looking like this:

```
[root@localhost ~]# cat /etc/motd
     _              _ _     _
    / \   _ __  ___(_) |__ | | ___
   / _ \ | '_ \/ __| | '_ \| |/ _ \
  / ___ \| | | \__ \ | |_) | |  __/
 /_/   \_\_| |_|___/_|_.__/|_|\___|

 FQDN:    localhost.localdomain
 Distro:  CentOS 6.6 Final
 Virtual: YES
 CPUs:    1
 RAM:     0.49GB

```


Role variables
--------------

- `motd_ascii_art`: ASCII art shown at the beginning of the motd.
- `motd_info`: List of additional information to show under the ASCII art. Look
into the `defaults` for an example.


License
-------

MIT


Author
------

Jiri Tyr

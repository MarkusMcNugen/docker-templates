[githubownerurl]: https://github.com/MarkusMcNugen
[preview]: https://raw.githubusercontent.com/MarkusMcNugen/docker-templates/master/sftp/SFTP.png "SFTP logo"

# Unraid SFTP server template

![SFTP logo][preview]

A hardened OpenSSH SFTP server with chroot jails and fail2ban, in one container, with an admin web UI and an optional file browser.

The template runs `markusmcnugen/sftp:2` with SFTP on host port 2222, since Unraid's own SSH server listens on 22, the admin web UI on over HTTPS on port 8443, and `/config` in `/mnt/user/appdata/sftp`. It adds the `NET_ADMIN` and `NET_RAW` capabilities, which fail2ban and the country rules need to block addresses.

On first start the container's log prints a setup link for the first admin, which works once, for one hour. Change the server's settings in the web UI rather than adding variables to the template: a variable set in the template wins over the web UI's Settings page, even when it is empty.

Coming from the 1.x image: [How To Upgrade From 1.x](https://markusmcnugen.github.io/docker-sftp/docs/how-to/upgrade-from-1x/).

# URLs

Docker maintainer: [MarkusMcNugen][githubownerurl]

Documentation: https://markusmcnugen.github.io/docker-sftp/

Docker Hub: https://hub.docker.com/r/markusmcnugen/sftp/

GitHub: https://github.com/MarkusMcNugen/docker-sftp

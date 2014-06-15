loguptime
=========

Does what it says on the tin, basically. Logs system uptime in a reasonably
simple but readable format. Uses `uptime`.

`loguptime.service` belongs in `/etc/systemd/system/` because AFAIK, that's
where custom services go.
`loguptime` can go anywhere (it's a simple bash script) but I put it in
`/usr/local/lib/systemd/system/scripts/` because that seemed reasonable. I
didn't want it in the `$PATH`, as it shouldn't be run more than once per boot.

Places its log in `/var/log/loguptime/log`. You should create that directory
first, else you might get errors.

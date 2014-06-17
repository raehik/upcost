upcost
=========

`upcost` logs uptime along with approximate power consumption and the cost of
that power.

`upcost.service` belongs in `/etc/systemd/system/` because AFAIK, that's
where custom services go.  
`upcost` is the script and can go anywhere, but I put it in
`/usr/local/lib/systemd/system/scripts/` because that seemed reasonable. I
didn't want it in the `$PATH`, as it shouldn't be run more than once per boot.

Places its log in `/var/log/upcost/log`. You should create that directory
first, else you might get errors.

Soon enough I'll write a script `upcost` which shows your 'outstanding debt'
as it were. I might have to change the name of the `upcost` script for that
(`upcost` makes most sense to me as asking the computer what the cost is). When
it is paid, the log is rotated.

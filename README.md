# restic-backup-docker-wol

A Docker container to automate [restic backups](https://restic.github.io/), based on the [one made by Lobaro](https://github.com/lobaro/restic-backup-docker). The single change made is the addition of the `awake` package so hooks (namely the `pre-backup.sh` one) can wake other server(s) on LAN using Wake-On-LAN (WOL).

Look at [my own pre-backup hook](https://github.com/snyssen/infra-snyssen.be/blob/master/roles/container_restic/files/local/pre-backup.sh) for an example of how to awake the backup server before running the backup.

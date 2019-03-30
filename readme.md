# Deploy from Gitlab using LFTP

Using FTP programs to add every change in your repository is not only  annoying but also time-very consuming. Fortunately, there's way to automate this flow with Gitlab Pipelines.

It allows you to  build, test and deploy committed code without any effort.

### LFTP Options
```
Mirror specified remote directory to local directory

 -c, --continue         continue a mirror job if possible
 -e, --delete           delete files not present at remote site
     --delete-first     delete old files before transferring new ones
 -s, --allow-suid       set suid/sgid bits according to remote site
     --allow-chown      try to set owner and group on files
     --ignore-time      ignore time when deciding whether to download
 -n, --only-newer       download only newer files (-c won't work)
 -r, --no-recursion     don't go to subdirectories
 -p, --no-perms         don't set file permissions
     --no-umask         don't apply umask to file modes
 -R, --reverse          reverse mirror (put files)
 -L, --dereference      download symbolic links as files
 -N, --newer-than=SPEC  download only files newer than specified time
 -P, --parallel[=N]     download N files in parallel
 -i RX, --include RX    include matching files
 -x RX, --exclude RX    exclude matching files
                        RX is extended regular expression
 -v, --verbose[=N]      verbose operation
     --log=FILE         write lftp commands being executed to FILE
     --script=FILE      write lftp commands to FILE, but don't execute them
     --just-print, --dry-run    same as --script=-
```
When using -R, the first directory is local and the second is remote.
If the second directory is omitted, basename of first directory is used.
If both directories are omitted, current local and remote directories are used.

# Rancher Dumper

When using rancher for software defined infrastructure,
the deployment may be changed manually from time to time using
the rancher CLI or the web dashboard. To still have the recent
state as a backup, exporting the full setup to a version control 
system may be useful.

This rancher dumper exports the rancher and docker compose files for
all stacks and optionally pushes them to a git repository.

Usage:
```
# source your rancher credentials
source /opt/rancher/creds.env

# export and sync with git repo
./gitsync path_to_git_repo

# export only
./stackdump path_to_output
```


## TODOs

 - [ ] extend exports: certificates, etc.
 - [ ] ship as container, to run rancher-dumper as started-once service in rancher
 
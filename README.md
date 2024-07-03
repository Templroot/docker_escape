# docker_escape
```
.\docker_escape                             Display usage information.

Checks:
.\docker_escape check                       Determine if the environment is a Docker container.

Automatic escape:
.\docker_escape auto                        Attempt automatic escape. If successful this starts a privileged container with the host drive mounted at /hostOS.

Manual escape techniques:
.\docker_escape unix                        Attempt an escape using a mounted Docker UNIX socket located at /var/run/docker.sock
.\docker_escape network                     Attempt to escape via Docker TCP socket if found on any interfaces. Port scans if network namespace shared with host.
.\docker_escape device                      Attempt to mount and chroot host OS filesystem. (i.e. if container uses --privileged or --device)
.\docker_escape cve-2019-5736  <payload>    Attempt CVE-2019-5736 (runC escape). If successful, this will trigger when a user runs an EXEC command and will corrupt the host runC binary.
```

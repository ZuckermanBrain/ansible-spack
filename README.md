app-spack
=========

A role that installs the Spack package manager.  Only supported on Debian and RHEL-based platforms.

Role Variables
--------------

`spack_repo` (string) : The HTTPS URL for main Spack git repo` (should be https://github.com/spack/spack.git unless you're operating off of a fork).
`spack_ver` (string) : The Spack version encoded as a Github tag.
`spack_service_user` (string) : A service account user.
`spack_service_user_uid` (int) : The UID for the service account user.  This is specified to ensure that the local service user account has the same UID across nodes in a clustered environment.
`spack_service_group` (string) : The primary group of the service account user.
`spack_service_group_gid` (string) : The GID for the service account user's primary grup.  This is specified to ensure that the local service user account uses the same GID across nodes in a clustered environment.
`spack_timeout_seconds` (int) : Timeout period when Spack is installing packages or populating a mirror.  Specified in seconds.
`spack_make_sys_default` (boolean) : Whether or not to add spack to the global shell path.
`spack_install_dir` (string) : Path to the directory where Spack is to be installed.
`spack_mirror_dir` (string) : A filesystem path where a package mirror should live.  Used to create a package mirror on the local filesystem.
`spack_mirror_pkgs` (list) :A list of packages to populate the source code cache / mirror with.
`spack_mirror_remote` (boolean) : Whether or not to configure a remote Spack mirror.
`spack_mirror_remote_addr` (string) : Used to define a remote mirror / source code code.  This should be populated with a protocol and FQDN` (e.g., https://example.com/mirror).
`spack_mirror_remote_name` (string) : A name for the remote mirror.
`spack_base_env` (string) : A list of packages to install in the Spack environment after it is created.
`spack_modules` (boolean) : Whether or not an environment modules system` (such as tcl / lmod) is used.

License
-------

Revised 3-Clause BSD License

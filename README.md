**deps** - parser script for automatically installing `BuildRequires` packages from files `*.spec`

The script is useful at the stage of rebuilding or backporting RPM packages of Mageia Linux or Fedora. It automatically detects the build dependencies (`BuildRequires`) that are described in `*.spec` and tries to install them. In the second step, it checks for the packages required during the installation of the package that is being rebuilt (`Requires`, `Recommends`).

For convenience, you need to place the script in `/usr/bin/deps`. Now just go to `/root/rpmbuild/SPECS` and give the command `deps` or `deps file_name.spec`.

Made and tested in Mageia Linux-8.

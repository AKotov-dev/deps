**deps** - parser script for automatically installing `BuildRequires` packages from files `*.spec` without `rpmspec`.  
  
The script is useful at the stage of rebuilding or backporting RPM packages of Mageia Linux or Fedora. It automatically detects the build dependencies (`BuildRequires`) that are described in `*.spec` and tries to install them. In the second stage, `dnf` is used to check for the presence of packages listed in the `Requires` and `Recommends` fields of the package being rebuilt.  
  
For convenience, you need to place the script in `/usr/bin/deps`. Now just go to `/root/rpmbuild/SPECS` and give the command `deps` or `deps file_name.spec`.
  
Made and tested in Mageia Linux.

A module is a package with streamlined deployment to a Viam server. 

Modules can run alongside viam-server as separate processes, communicating with viam-server over UNIX sockets.
A module can simply represent a package of artifacts/files/packages which needs delivery.


List the contents of the tarball:

tar -tzvf examplePackage.tar.gz

Breakdown of the command:

-t: List the contents of the archive.
-z: Filter the archive through gzip.
-v: Verbosely list files processed.
-f: Specify the filename of the archive.

Extract the tarball to verify its contents:

tar -xzvf examplePackage.tar.gz -C /path/to/extract/directory
Breakdown of the command:

-x: Extract the contents of the archive.
-z: Filter the archive through gzip.
-v: Verbosely list files processed.
-f: Specify the filename of the archive.
-C: Specify the directory to extract the files to.
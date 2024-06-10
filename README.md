# Example of a Package Deployment Module

A module is a package with streamlined deployment to a Viam server. 

- Modules can run alongside viam-server as separate processes, communicating with viam-server over UNIX sockets.
- A module can also simply represent a package of artifacts/files/packages which needs delivery. This module does not start up a process.

The package gets deployed at:

`{user directory}/.viam/packages/.data/module/{org id of user managing package}-{package name}-{version}-{OS}-{device architecture}`

## This Example's Package Contents
- **Dockerfile**: Builds container images.
- **exampleConfig.json**: JSON configuration file.
- **exampleConfig.yaml**: YAML configuration file.
- **exampleEnv.env**: Environment variables file.
- **examplePython.py**: Python script.
- **exampleRequirements.txt**: Python dependencies.
- **exampleService.service**: System service unit file.
- **exampleShell.sh**: Shell script.
- **examplePackage.tar.gz**: Archive containing all the listed files.

Once deployed a user can interact with the package with the following commands to verify deployment.

### List the contents of the tarball:
```sh
tar -tzvf examplePackage.tar.gz
```
#### Breakdown of the command:

- -t: List the contents of the archive.
- -z: Filter the archive through gzip.
- -v: Verbosely list files processed.
- -f: Specify the filename of the archive.

### Extract the tarball to verify its contents:

```sh
tar -xzvf examplePackage.tar.gz -C /path/to/extract/directory
```
### Breakdown of the command:

- -x: Extract the contents of the archive.
- -z: Filter the archive through gzip.
- -v: Verbosely list files processed.
- -f: Specify the filename of the archive.
- -C: Specify the directory to extract the files to.

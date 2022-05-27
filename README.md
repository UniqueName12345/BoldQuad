# BoldQuad
Imagine LibreWolf but with more updates and less guarantees? Yeah, this is it.

### Important

The build scripts are currently meant to be run in a CI environment with Docker containers
and gitlab-runners. Updated instructions for local builds or setting up your own
appropriate runners will be provided again in the future.

### How to Install
Since there are currently no releases, you need to clone the repository and build it yourself using Docker.

Step 1: Install Docker.

In order to do this, you need to have Docker installed. (this tutorial assumes you have a arch based system)

```
sudo pacman -S docker
```

This command will install Docker using the official package manager.

Step 2: Make a new directory and clone the repository.

```
mkdir ~/bq (or any other directory you want)
cd ~/bq (this is the directory you want to clone the repository to)
git clone https://github.com/UniqueName12345/BoldQuad
```

This command makes a new directory and clones the repository into it.

Step 3: Make a docker image.

```
cd ~/bq/BoldQuad
docker build -t boldquad .
```

This command builds a docker image from the repository.

Step 4: Run the docker image.

```
docker run -it --rm -v /home/user/path/to/bq/BoldQuad:/bq boldquad
```

This command runs the docker image.

### And now, the fun begins!

Step 5: Run the install dependencies script.

```
cd ~/bq/BoldQuad/scripts
./1_Install_Dependencies.sh
```

Step 6: Wait for the installation to finish, then run the download source code script.

```
./2_Download_Source_Code.sh
```

Step 7: Wait for the download to finish, then run the configure script.

```
./3_Configure_Source_Code.sh
```

Step 8: Wait for the configure to finish, then run the build binary tarball script.

```
./4_Build_Binary_Tarball.sh
```

Step 9: Wait for the build to finish, then run the configure binary tarball script.

```
./5_Configure_Binary_Tarball.sh
```

Step 10: Once that's done, you can run launch_librewolf.sh to launch LibreWolf.

```
cd ~/bq/BoldQuad/content
./launch_librewolf.sh
```
### Other builds
Currently none! If you want a build, please open an issue or pull request.
In the meanwhile, if you want a windows version, you can run WSL with Docker.


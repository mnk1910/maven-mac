# How to install manually `Maven` on your Mac

All the bellow commands are command line commands and they need to be executed ONLY in `terminal`.

1. Download `maven`

```
curl -O http://apache.mirrors.spacedump.net/maven/maven-3/3.5.2/binaries/apache-maven-3.5.2-bin.tar.gz
```

2. Move the newly downloaded archive to the standard location where the software is locally installed

```
sudo mv apache-maven-3.5.2-bin.tar.gz /usr/local
```

_**Important note**_: you will be asked to enter your username password (the one you're using to login to your computer)

3. Extract the content of the archive downloaded above

```
tar xfvz apache-maven-3.5.2-bin.tar.gz
```

4. Adjust the environment variables used by `maven` and make them permanent
```
vim ~/.bashrc
```

5. Press `i` on your keyboard to enter into `INSERT` mode (you will see _-- INSERT --_ in the bottom left corner) and using the arrow keys on your keyboard go to the end of the file and paste the following lines:

```
export M2_HOME=/usr/local/apache-maven-3.5.2
export PATH=$PATH:$M2_HOME/bin
```

6. Press `esc` on keyboard to exit the `INSERT` mode and then `:wq` to save and exit the file

7. Load the changes

```
source ~/.bashrc
```

8. Test if your `maven` installation works

```
mvn -version

Maven home: /usr/local/apache-maven-3.5.2
Java version: 1.8.0_152, vendor: Oracle Corporation
Java home: /Library/Java/JavaVirtualMachines/jdk1.8.0_152.jdk/Contents/Home/jre
Default locale: en_SE, platform encoding: US-ASCII
OS name: "mac os x", version: "10.13.1", arch: "x86_64", family: "mac"
```

If you can't see the output above something went wrong at one of the steps and you will need to start over

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

# mobox-builds
Automatic builder for mobox written in the modern way.

The repository builds Wine automatically for Mobox using CI.

Revision 0001

Script that is used for manually installing Wine into `wine-ge-custom` container:

```bash
cd $PREFIX/glibc
rm -rf $PREFIX/glibc/wine-ge-custom
tar -xvf $HOME/storage/downloads/wine-9.0-custom-amd64.tar.xz
mv $PREFIX/glibc/wine-9.0-custom-amd64 $PREFIX/glibc/wine-ge-custom
rm -rf $PREFIX/glibc/opt/scripts/start-tfm
cp $HOME/storage/downloads/start-tfm $PREFIX/glibc/opt/scripts
cd ~
mobox
```

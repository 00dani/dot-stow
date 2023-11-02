# dot/stow

This is a prebuilt distribution of GNU Stow, based on [my slightly modified fork](https://git.00dani.me/00dani/stow), which has been built to use relative paths for locating Perl modules at runtime. It's perfect for cloning into your ~/dotfiles and using with no further steps, since it doesn't care what your home directory is called and will work no matter where you put it.

To build this version of Stow for yourself (or, more likely, if you're me and need to update the build when Stow changes upstream):

```bash
git clone https://git.00dani.me/00dani/stow
cd stow
autoreconf -iv
./configure --enable-relative --prefix=$PWD/out --with-pmdir=$PWD/out/lib/perl PERL=/usr/bin/perl
make
make install
```

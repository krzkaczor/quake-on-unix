# Quake-on-unix
How to get Quake running on linux / mac

This tutorial is focused on mac but exactly the same commands should work on any linux system.

## Get original .pak game files
You can buy Quake on [gog.com](https://www.gog.com/game/quake_the_offering)

### Unpacking
GOG provides `.exe` file which obviously doesn't play nice with everything else then windows. To unpack it use `innoextract`. Unfortunately `brew` version segfaults during unpacking game files that's why we will need to build it from sources.

```
git clone https://github.com/dscharrer/innoextract.git .
cd innoextract
mkdir -p build
cmake .
```

Now all you need to do is point to `exe` file.

```
 ./build/innoextract ../../setup_quake_the_offering_2.0.0.6.exe
```


## Run it with Quake runner for your platform

Just google for `Quake X` or something similar. Point it to `.pak` files and you're done.
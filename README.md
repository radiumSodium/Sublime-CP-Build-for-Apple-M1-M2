# Sublime-CP-Build-for-Apple-M1-M2

This will fix the g++ compilation error on Apple silicon processor

used to love sublime text as my code editor for Competitive Programming. Specially because I has special build system which helped me taking Input from the `inputf.in` file and showing output to
`outputf.in` file. and the compilation was easy just a shortcut away `shift + command + B` . After buying my new Apple M1 Pro the compilation of C++ file with g++ compiler was not working properly. I kind of left coding C++ on M1 pro. Now I have the solution to this and I thought I should share with all.

## Here is the sublime system I was talking

![sublime](/images/Sublime.png)

### There is the Custom build system:

```bash
{
    "cmd": ["g++ -std=c++11 $file_name -o $file_base_name && ./$file_base_name<inputf.in>outputf.in"],
    "selector": "source.c++",
    "shell": true,
    "working_dir": "$file_path"
}
```

# If you want to run g++ compiler on Apple silicon processor

1. First of all install Home brew
1. Install gcc from homebrew
1. check if the gcc and g++ is available to you computer by these command:

```zsh
gcc-11 --version
g++-11 --version
```

here `gcc-11` and `g++-11` refers to the gcc version 11 if the version is different say for example version 9 then the command will be

```zsh
gcc-9 --version
g++-9 --version
```

these will retun output simmilar to this if gcc and g++ is installed

```
gcc-11 (Homebrew GCC 11.4.0) 11.4.0
Copyright (C) 2021 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

```
g++-11 (Homebrew GCC 11.4.0) 11.4.0
Copyright (C) 2021 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

# For compile with g++ in terminal

you have to add `-std=c++11` to get the complilation done with g++

here is the full command to compile a c++ file

```
g++ -std=c++11 primsAlgo.cpp
```

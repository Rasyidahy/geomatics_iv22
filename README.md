# Geomatics_iv22
>Do submit your assignment as a Git repository and please include a README.md file to explain on how
to run the application

***Some criteria’s that we will evaluate upon (in no particular order):***
```
 -Your approach to the problem
 -Use of Object Oriented programming, SOLID principles or other programming paradigm
 -Clean handling of error & input problem
 -Accuracy of the result
 -Bonus marks: Can handle input without comma
```

![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/task%20geomatics.jpg)

The task is develop a console program to tokenize a free form text into address components. For this assessment, I am currently using **libpostal**, **MSYS2**, **C** and **Python** for run the address.

# Libpostal
For this assessment, i use open source tool libpostal to pare out tructured information from the full address. The core library of libpostal is written in C while supports language binding for Python, Java, PHP and NodeJS. libpostal is a C library for parsing/normalizing street addresses around the world using statistical NLP and open data.

# Libpostal configure
![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/libpostal%20config.jpg)

# Installation (Windows)
For window, i install the MSys2 from http://msys2.org. MSYS2 ("minimal system 2") is a software distribution and a development platform for Microsoft Windows, based on Mingw-w64 and Cygwin, that helps to deploy code from the Unix world on Windows. It plays the same role the old MSYS did in MinGW.

![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/35e09212ef118a86bbc82d800d60335f6ea48176/6759993.png)

For running Msys2:
```
pacman -Syu
```

For install the following prerequisites:
```
pacman -S autoconf automake curl git make libtool gcc mingw-w64-x86_64-gcc
```

Then to build the C library for libpostal:
```
git clone https://github.com/openvenues/libpostal
 cd libpostal
 cp -rf windows/* ./
 ./bootstrap.sh
 ./configure 
 make -j4
 make install
 ```
 # Bindings
**Libpostal** is designed to be used by higher-level languages. For this assessment, i choose to binding libpostal with Python languages.

**pypostal** is the official Python binding for libpostal, a fast statistical parser/normalizer for street addresses anywhere in the world.

After install the libpostal C library, then we can install the **pypostal**. For window, i install below code. 

```
sudo apt-get install curl autoconf automake libtool python-dev pkg-config
```
To install the Python library, i run:
```
pip install postal
```

# Example of Parsing
This example parse results are taken from the interactive address_parser program that builds with libpostal when run `make` 

![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/libpostal%20make.jpg)

# Make install
![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/libpostal%20make%20install.jpg)

# Command-line usage (expand)
After building libpostal:

```
cd libpostal

cd src/

./libpostal "Quatre vingt douze Ave des Champs-Élysées"

```
![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/65f0fa9e131802b0427d6c1f0a9194e2c9f01835/libpostal%201.png)

# Command-line usage (parser)
After building libpostal:

```
cd src/

./address_parser

```
address_parser is an interactive shell. Just need to type addresses and libpostal will parse them and print the result.

![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/libpostal%20addresee_parser%20output.jpg)

# Assignment
> **By full address**
![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/libpostal%20addresee_parser%20output.jpg)

> **By User input can contains incomplete address, mean each address component is optional**
![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/libpostal%20addresee_parser%20output.jpg)

> **By handle input without comma**
![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/libpostal%20addresee_parser%20output.jpg)



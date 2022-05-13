# geomatics_iv22
Develop a console program to tokenize a free form text into address components. For this assessment, I am currently using **libpostal**, **MSYS**, **C** and **Python** for run the address.

![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/task%20geomatics.jpg)

# Libpostal
For this assessment, i use open source tool libpostal to pare out tructured information from the full address. The core library of libpostal is written in C while supports language binding for Python, Java, PHP and NodeJS. libpostal is a C library for parsing/normalizing street addresses around the world using statistical NLP and open data.

# Installation (Windows)
For window, i install the MSys2 from http://msys2.org. MSYS2 ("minimal system 2") is a software distribution and a development platform for Microsoft Windows, based on Mingw-w64 and Cygwin, that helps to deploy code from the Unix world on Windows. It plays the same role the old MSYS did in MinGW.

![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/9ffd8f22ab87d9d98c2f1fcf09e52151ad41b906/task%20geomatics.jpg)


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

![This is an image](https://github.com/Rasyidahy/geomatics_iv22/blob/3ef6f45714ec6795fe35a016aa78344430c10982/one.jpg)

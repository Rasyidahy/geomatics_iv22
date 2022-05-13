# geomatics_iv22
Develop a console program to tokenize a free form text into address components. For this assessment, I am currently using libpostal, MSYS and Python for run the address.
# Libpostal
For this assessment, i use open source tool libpostal to pare out tructured information from the full address. The core library of libpostal is written in C while supports language binding for Python, Java, PHP and NodeJS. libpostal is a C library for parsing/normalizing street addresses around the world using statistical NLP and open data.
# Installation (Windows)
For window, i install the MSys2 from http://msys2.org. MSYS2 ("minimal system 2") is a software distribution and a development platform for Microsoft Windows, based on Mingw-w64 and Cygwin, that helps to deploy code from the Unix world on Windows. It plays the same role the old MSYS did in MinGW.
Then to build the C library:

```git clone https://github.com/openvenues/libpostal
 cd libpostal
 cp -rf windows/* ./
 ./bootstrap.sh
 ./configure 
 make -j4
 make install

## Contents
1) Introduction
2) Building with autoconf/automake
3) Contact

---------------
### 1) Introduction

JSBSim is a multi-platform, general purpose object-oriented Flight
Dynamics Model (FDM) written in C++. Jon Berndt and Tony Peden began
about mid-1998 writing JSBSim. As of this writing it is the default
FDM for FlightGear. JSBSim can also be run in a standalone batch mode
for testing and study. More information on JSBSim can be found at the
JSBSim home page here:

http://www.jsbsim.org

---------------
### 1) 简介
JSBSim是一个跨平台的C++飞行气动模型。由Jon Berndt和Tony Peden在1998年年中开始进行开发。最初JSBSim是作为FlightGear的气动模型。同时，JSBSim也能作为独立程序以命令行模式运行，用于测试和学习。更多有关JSBSim的信息能够在官网上找到：

http://www.jsbsim.org

* 在本git仓库中，由kevinSWAT继续进行二次修改，以用于本人的其他项目。
----------------------------------
### 2) Building with autoconf/automake


Unpack the distribution tarball (if needed - CVS users will have
downloaded the code directly) using your preferred method, and change
to the working directory. For example :

$ tar xvfz JSBSim-0.1.2.tar.gz
$ cd JSBSim-0.1.2

NOTE for CVS users: If you are using JSBSim from a CVS checkout, or
snapshot, you will need to create the initial configure script. The
commands to do this have been included in the 'autogen.sh' script, so
just :

$ ./autogen.sh [--no-configure]

If you wish to customise your version of JSBSim, use the following to
determine any build-time options you may be interested in.

$ ./configure --help

Then :

$ ./configure

This will check your system platform, compiler and other local
configuration variables needed to build JSBSim, and generates the
necessary Makefiles. Next :

$ make

Will compile the various classes, and build the JSBSim application.

* 建议使用cmake进行构建
----------------------------
### 3) Building JSBSim libraries


By default, the JSBSim libraries are not built. To build and install
the libraries, use:

$ ./autogen --enable-libraries [--disable-static] [--enable-shared]

The configure options can be used to select what libraries to build.

$ make install

Unless specified otherwise (with --prefix configure option), this will
install JSBSim libraries into '/usr/local/lib' and JSBSim headers
into '/usr/local/include/JSBSim'.


----------
### 4) Contact


For more information on JSBSim contact Jon Berndt at jon@jsbsim.org.



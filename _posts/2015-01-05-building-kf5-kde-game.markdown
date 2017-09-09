---
layout: post
title:  "Building KF5 KDE Game "
date:   2015-01-05 14:34:25
tags: SoK KDE Tech
---

My journey in SoK (Season of KDE) 2014 has been official ended. While I was working in KDE-Games I found that there is no such guide on how to build and get started with development of KDE-Games. So I have written a small guide on how to set-up building environment for KDE-Games based on my experience in SoK 2014. I would love to share it with the KDE members.


Building KF5 KDE Game

Introduction

As we all know KDE apps are being ported to KF5, same goes with kdeGames. In this doc, I will discuss the compilation and installation of KDE game application that is ported to kf5.
I recommend you to go through “Getting started Page” before reading this doc.

Steps

Install Qt 5.x. For more info about installing Qt 5.x, go to Qt official Page. You might need to export the Qt path if it is installed in a local directory. Simply put the mentioned lines in your .profile or bashrc file.

PATH=/Path/to/Qt5/gcc_64/bin:$PATH
export PATH

You need to install kf5.  It can either be built or it’s binaries can be installed. For more info about building, refer here and for binaries, look here. In addition to it, framework’s components might be needed. Again, you can either get it build or install the binaries. For information about building them, look here and for debian based systems, you can easily install binaries using any package manager.

Once you are finished installing Qt 5.x and kf5, next thing you need is a KF5KDEGames package (Ported version of libkdegames).

First, you have to clone the code of libkdegames:

    git clone git://anongit.kde.org/libkdegames.git

This will create a directory with libkdegames source code inside.

    cd libkdegames

Checkout it’s frameworks branch

    git checkout frameworks

Make a build directory where you will be building KF5KDEGames

    mkdir build && cd build

Then, you need to build and compile it.

    cmake .. -DCMAKE_INSTALL_PREFIX=<install_path> -DCMAKE_BUILD_TYPE=debugfull
    make

Once you have a successful compilation of KF5KDEGames, now let’s install it (you may need root privileges for installing it).

    sudo make install

If you are having an application that is based on qml, then, you may also have to export QML2_IMPORT_PATH. For example:

    QML2_IMPORT_PATH=/usr/local/lib/x86_64-linux-gnu/qml
export QML2_IMPORT_PATH

Once you are through with these requirements, you can build and run your KDE games application. All the applications under the KDEgames can be found here.

For instance, let’s build knetwalk. The repository for it’s source code can be found here.

    git clone git://anongit.kde.org/knetwalk
    cd knetwalk

Applications ported to kf5 are present in frameworks branch. We have started merging frameworks branch with the master branch. So, please have a look if master branch contains the ported app.

    git checkout frameworks

Now we will make a “build” directory and get started with building the app knetwalk

    mkdir build && cd build
    cmake ../

Now we start compiling the code

    make

You can also use make -j4 for multiprocessing and increasing the compiling speed.
Once we have a clean compile, it’s time to install knetwalk (you might need root privileges for this).

make install

With this, we have installed knetwalk (ported to kf5).

Debugging

You might come across “ecm package not available”. Here, this “ecm package” means extra-cmake-modules package. You may get errors while building (cmake ../) about not finding a particular package. Every app has it’s own dependencies.So, please have a look and fulfill all the dependencies to get rid of errors.

You can always ask your queries on IRC (#kde-devel and #kde-games) and mailing lists (kde-devel and kde-games-devel).

Refer for more details at this [doc Link](https://docs.google.com/document/d/1B9hQ0Ry-H-RKz9kRWG_P_2KTgwTMalvtO7YpME6dwfY/edit?usp=sharing)


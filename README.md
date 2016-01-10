# linux-lib-reference

A quick reference to checkout what lib/pkg is missing when you failed to compile your c programs

## Problem & Target

Did you ever encounter an error message like this when you try to compile a program with gcc? 

    main.c:13:17: fatal error: usb.h: No such file or directory  
    #include <usb.h>
    compilation terminated. flashprog.c:14:17: fatal error: usb.h: No such file or directory"

This repo is build to give you a fast reference to checkout what library/package is missing when you failed to compile your c/c++ program source.

## How to use this repo

Let's say, you have an compile error with your ubuntu system, then you can open `[your-linux-system].md` to search if there is any entry related to you missing include file. If yes, use the command right below the error message to install the missing pkg.

Eg, when you compile a driver, and you got the following message within your ubuntu system.

    main.c:13:17: fatal error: usb.h: No such file or directory  
    #include <usb.h>
    compilation terminated. flashprog.c:14:17: fatal error: usb.h: No such file or directory"

Then you can open `ubuntu.md`, and search `usb.h`. Then you should find a line related this file. And then you can run an `apt-get` command to install the missing `libusb-dev` package like this:

    sudo apt-get install libusb-dev

## Contribute

First, create a new line for the problem:

    #include <header.h>, [header.h]: No such file or directory
    
Second, create a new line right below for the solution

    #sudo apt-get install <the-solution-package>


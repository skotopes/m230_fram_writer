# About

This software allows to program FRAM memory connected to MSP430 CPU.


# Toolchain

If you use MacOS or Linux then it is as simple as:

    make tc

This command will pull official mspgcc toolchain to toolchain folder. 
If you have any other OS or want some other toolchain options, then consult Makefile.


# Compiling

Just

    make


# Generating payload

You'll need srecord installed. 

Put your fram_data.bin in this folder and execute following command:

    srec_cat fram_data.bin -Binary -output fram_data.c -C-Array fram_data

this will generate include file for you. Than just type `make` and that's it.

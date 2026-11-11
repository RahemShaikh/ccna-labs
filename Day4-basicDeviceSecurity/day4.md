# Lab 04 - CLI Configuration

## Overview

Use the CLI to change permission space, add and encrypt passwords/secrets, and saving configurations 

**Includes:** 1 switch, 1 router, 3 PCs

## Objectives

* Change hostname
* Change EXEC modes
* Enable password/secrets
* Encrypt password
* Save config file
  
## Topology

<img width="858" height="359" alt="image" src="https://github.com/user-attachments/assets/f16ab9cf-13e3-48f1-bc21-f57127d538d5" />

## Changing hostname and enabling unencrypted password for priveleged access mode

<img width="1722" height="224" alt="image" src="https://github.com/user-attachments/assets/0db0929a-c893-410e-9d45-7ee4ce74c54c" />

## Display running configuration

<img width="1414" height="595" alt="image" src="https://github.com/user-attachments/assets/8bea124c-b2f5-4cd5-816e-6a6ce63d222e" />

## Enabling password encryption and secret password

<img width="1474" height="418" alt="image" src="https://github.com/user-attachments/assets/b97ff0a5-445b-45d0-a278-6eb82b3dc10a" />

## Setting up startup config file

<img width="576" height="373" alt="image" src="https://github.com/user-attachments/assets/1dee417f-aa5c-4c30-973f-8a5327483228" />

## Commands Used

* ```enable```: switch from user mode to privileged mode          
* ```configure terminal```: switch from privileged mode to global configuration mode
* ```hostname```: change hostname of device
* ```enable password```: create unencrypted password to enter privileged mode
* ```service encrypt-password```: encrypt password
* ```enable secret```: creates a more secure encrypted password that override passwrod
* ```do```: to use privileged commands in global configuration mode
* ```show```: displays config files
* ```copy```: save running config file to startup config file

## What I Learned

* If you type a command not recognized by the CLI it might think it is a host name and translate using DNS; To get out of this use ctrl+shift+6
* You can only enable password encryption in global configuration mode
* You can only display running config file in privileged access mode or using the do command in global configuration mode
* Password and secret can not be the same
* Down arrow lets you go all the way down the CLI

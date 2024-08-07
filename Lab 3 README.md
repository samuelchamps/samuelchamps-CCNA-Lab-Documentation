# Basic Device Security
## Types of mode
- User exec mode
- Priviledge exec mode
- global exec mode

### User EXEC Mode:

This is the default mode when you first log into the CLI.
It provides basic monitoring commands.
The prompt is Router>.

### Privileged EXEC Mode:

This mode allows access to all commands and features.
To enter this mode, you use the enable command.
The prompt changes to Router#.

### Global Configuration Mode:

This mode is used to configure global settings on the device.
Entered from Privileged EXEC mode using the configure terminal command.
The prompt changes to Router(config)#.

## Enable Password and Enable secret
the concepts of enable password and enable secret are important for securing access to Privileged EXEC mode on Cisco devices. 

### Enable Password:
The enable password command sets a password that is required to access Privileged EXEC mode.
This password is stored in the configuration in plain text, making it less secure. You can use the service password encryption to encrypt it.

### Enable Secret:

The enable secret command sets an encrypted password for access to Privileged EXEC mode.
It is more secure because the password is stored in the configuration in an encrypted form.
If both enable password and enable secret are set, the enable secret takes precedence.

# Configuring Enable Password and Enable Secret

## Purpose
Secure access to Privileged EXEC mode using `enable password` and `enable secret`.

## Configuration Steps

### Setting `enable password`
- **Description:** Sets a plain text password for Privileged EXEC mode.
- **Command:**
  ```plaintext
  Router> enable
  Router# configure terminal
  Router(config)# enable CCNA
  Router(config)# service password encryption
  Router(config)# exit
  Router#

### Result
![Screenshot (78)](https://github.com/user-attachments/assets/aea61cdb-76a8-4f7d-89be-abc443ffa226)

### Setting `enable secret`
Description: Sets an encrypted password for Privileged EXEC mode.
```plaintext
Router> enable
Router# configure terminal
Router(config)# enable secret your_secret_password
Router(config)# exit
Router#
```
### Result

![Screenshot (79)](https://github.com/user-attachments/assets/e523ba97-1cde-4536-8e1d-0f07334a03fe)

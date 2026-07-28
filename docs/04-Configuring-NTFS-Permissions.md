# Assigning NTFS Permissions

## Overview

NTFS permissions were configured to control access to files and folders stored on the Windows File Server. Permissions were assigned to security groups instead of individual users to follow common enterprise administration practices.

## NTFS Permissions

NTFS permissions control what users can do with files and folders after accessing the storage location.

Common NTFS permissions include:

- Read
- Write
- Modify
- Full Control

## Permission Design

The following permissions were assigned:

| Folder | Security Group | Permission |

| HR | GG-HR-Users | Modify |  
| Finance | GG-Finance-Users | Modify |  
| IT | GG-IT-Users | Modify |  
| Public | GG-All-Employees | Modify |  

## Configuration Steps

1. Opened folder properties
2. Navigated to the Security tab
3. Added department security groups
4. Assigned appropriate NTFS permissions
5. Verified permissions were applied

## Screenshots

### HR Folder Permissions

[![HR NTFS Permissions](path/to/image.png)](https://github.com/HarperSec/Windows-File-Server-Lab/blob/main/screenshots/06-HR%20NTFS%20Permissions.png)

### Finance Folder Permissions

[![Finance NTFS Permissions](path/to/image.png)](https://github.com/HarperSec/Windows-File-Server-Lab/blob/main/screenshots/05-Finance%20NTFS%20Permissions.png)

## Summary

NTFS permissions provide granular control over file and folder access. Assigning permissions through security groups creates a scalable and manageable access control structure.

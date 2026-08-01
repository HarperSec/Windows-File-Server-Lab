# Creating Security Groups

## Overview

Security groups were created to manage access to file server resources. Instead of assigning permissions directly to individual users, permissions will be assigned to groups. This follows common enterprise administration practices.

## Why Security Groups Are Used

Security groups simplify permission management by allowing administrators to control access for multiple users at once.

Example:

A user is added to the HR security group, and they automatically receive the permissions assigned to the HR department share.

## Groups Created

The following security groups were created:

| Group Name | Purpose |

| GG-HR-Users | Access to HR resources |  
| GG-Finance-Users | Access to Finance resources |  
| GG-IT-Users | Access to IT resources |  
| GG-All-Employees | Access to public resources |  

![Security Groups](../screenshots/04-Security%20Groups.png)

## Creating Security Groups

Steps completed:

1. Opened Active Directory Users and Computers
2. Created a File Server Groups organizational unit
3. Created department-based security groups
4. Configured groups as Global Security Groups
5. Added test users to appropriate groups

![Group Members](../screenshots/03-Group%20Members.png)


## Summary

Security groups provide a scalable method for managing access to shared resources. The next step is assigning NTFS permissions to these groups.

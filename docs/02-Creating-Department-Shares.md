# Creating Department Shares

## Overview

This section covers the creation of department-based shared folders on the Windows File Server. The goal is to simulate a business environment where different departments have dedicated storage locations.

## Folder Structure

The file server was organized using the following structure:  
├── HR  
├── Finance  
├── IT  
└── Public


## Creating Department Folders

The following department folders were created:

- HR
- Finance
- IT
- Public

These folders represent separate storage locations for different organizational departments.

![Department Folders](../screenshots/01-Department%20Folders.png)

## Configuring Folder Sharing

Each department folder was configured as a network share.

Steps completed:

1. Opened folder properties
2. Navigated to the Sharing tab
3. Selected Advanced Sharing
4. Enabled folder sharing
5. Configured initial sharing permissions

![Folder Sharing](../screenshots/02-Folder%20Sharing.png)
 

## Summary

Department shares provide centralized file storage while allowing organizations to separate resources based on business requirements. The next step is creating security groups to control access to these shared resources.

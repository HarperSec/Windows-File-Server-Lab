# Configuring Share Permissions

## Overview

Share permissions were configured for each department folder to allow users to access the shared resources over the network. In this lab, Share Permissions were kept simple by allowing **Everyone** Full Control, while NTFS permissions provide the primary layer of security.

## Understanding Share Permissions

Share permissions only apply when a user accesses a shared folder over the network. They work together with NTFS permissions, and the most restrictive effective permission determines what a user can do.

The available Share Permissions are:

* Read
* Change
* Full Control

## Configuration Steps

The following steps were completed for each department share:

1. Opened the folder properties.
2. Selected the **Sharing** tab.
3. Opened **Advanced Sharing**.
4. Verified **Share this folder** was enabled.
5. Opened **Permissions**.
6. Confirmed the **Everyone** group had **Full Control**.

![Advanced](../screenshots/07-Advanced%20Sharing.png)
![Share](../screenshots/08-Share%20Permissions.png)


## Share Configuration

| Shared Folder | Share Permission        |
| ------------- | ----------------------- |
| HR            | Everyone – Full Control |
| Finance       | Everyone – Full Control |
| IT            | Everyone – Full Control |
| Public        | Everyone – Full Control |


## Summary

Share permissions provide network-level access to shared folders. In this lab, Share Permissions were intentionally configured with broad access, while NTFS permissions enforce department-specific security. This layered approach reflects a common enterprise configuration for Windows File Servers.


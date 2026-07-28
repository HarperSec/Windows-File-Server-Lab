# Testing User Access

## Overview

After configuring NTFS and Share Permissions, user access was tested to verify that permissions were working as intended. Each user was able to access only the resources assigned to their department while being denied access to unauthorized department shares.

## Test Environment

The following test accounts were used:

| User        | Department             |  

| HRUser      | Human Resources        |  
| FinanceUser | Finance                |  
| ITUser      | Information Technology | 

## Access Test Results

| User        |  HR | Finance |  IT | Public |  

| HRUser      |  ✅  |    ❌    |  ❌  |    ✅   |  
| FinanceUser |  ❌  |    ✅    |  ❌  |    ✅   |  
| ITUser      |  ❌  |    ❌    |  ✅  |    ✅   |  

## Validation Process

The following steps were completed for each test account:

1. Signed in with the user account.
2. Connected to each shared folder.
3. Verified access to authorized department shares.
4. Verified access was denied to unauthorized department shares.
5. Confirmed access to the Public share.

## Screenshots

### Successful Department Access

[![Access Successful](path/to/image.png)](https://github.com/HarperSec/Windows-File-Server-Lab/blob/main/screenshots/09-HR%20Access%20Sucessful.png) 

### Access Denied

[![Access Denied](path/to/image.png)](https://github.com/HarperSec/Windows-File-Server-Lab/blob/main/screenshots/10-Access%20Denied.png)

## Summary

Testing confirmed that the configured NTFS and Share Permissions were functioning correctly. Users could access only the resources required for their roles, demonstrating the principle of least privilege and validating the security configuration of the Windows File Server.


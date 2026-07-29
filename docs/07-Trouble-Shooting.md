# Troubleshooting

## Overview

During the Windows File Server configuration process, several issues were encountered while testing user access. Troubleshooting involved reviewing Active Directory group membership, NTFS permissions, and Share Permissions to identify and resolve access control problems.


# Issue 1: Users Could Access Unauthorized Department Shares

## Problem

During access testing, department users were able to access and create folders within shares that did not belong to their assigned department.

Example:

- HRUser was able to create folders inside the Finance share.
- FinanceUser was able to access HR resources.
- ITUser was able to access other department shares.

This indicated that NTFS permissions were not correctly restricting access.


## Investigation

The following areas were reviewed:

### 1. Share Permissions

Verified that department shares were configured with:

Everyone → Full Control


This configuration was intentional based on the lab requirements. Share permissions were not the cause of the issue.



### 2. NTFS Permissions

Reviewed folder security settings:

Example:
Finance Share Permissions

CREATOR OWNER
SYSTEM
Administrator
GG-FINANCE-USERS
Users


The issue was caused by broad permissions assigned to:
Users

The Users group had permissions that allowed unauthorized accounts to create folders and modify files.


## Resolution

Updated NTFS permissions by removing unnecessary broad permissions and applying department-based security groups.

Example:

Before:
Finance Folder

Users → Modify
GG-FINANCE-USERS → Modify

After:
Finance Folder

GG-FINANCE-USERS → Modify
Administrators → Full Control
SYSTEM → Full Control


The same process was applied to HR and IT department shares.


# Issue 2: Unable to Remove Certain Permissions

## Problem

Some permissions entries could not be removed from department folders.

Example:
SYSTEM
CREATOR OWNER


---

## Cause

These permissions were inherited from parent folders or were required Windows system permissions.

---

## Resolution

Reviewed Advanced Security Settings and disabled inheritance when necessary. Retained required system permissions while removing unnecessary broad user access.

---

# Issue 3: User Access Testing Failed

## Problem

Initial testing did not match the expected results.

Expected:

| User | HR | Finance | IT |

| HRUser | ✅ | ❌ | ❌ |  
| FinanceUser | ❌ | ✅ | ❌ |  
| ITUser | ❌ | ❌ | ✅ |  

Actual results showed users had access to multiple department shares.


## Resolution

Reviewed:

- Active Directory group membership
- NTFS permissions
- Share permissions
- Folder inheritance

After correcting permissions, access testing confirmed users only had access to authorized department resources.


# Final Validation

After troubleshooting:

✅ HR users could access HR resources  
✅ Finance users could access Finance resources  
✅ IT users could access IT resources  
✅ Unauthorized department access was denied  
✅ Public share remained accessible to all users  


# Lessons Learned

This troubleshooting process demonstrated the importance of:

- Proper NTFS permission configuration
- Using security groups instead of assigning permissions directly to users
- Understanding the difference between Share and NTFS permissions
- Testing access using standard user accounts
- Applying the principle of least privilege

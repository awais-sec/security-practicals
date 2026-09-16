# File Permissions in Linux

## Project Description

Ensuring users on this team are authorized with the appropriate permissions helps keep the system secure and healthy. In this report, it's determined whether the current permissions match the authorization that should be given. Where they don't match, permissions need to be modified to authorize the appropriate users and remove any unauthorized access.

## Check File and Directory Details

I used `ls -al` to display all permissions and directories.

## Describe the Permissions String

`drwxr-xr-x`

- **Position 1 (File type):** `d` = Directory
- **Positions 2–4 (User/Owner):** `rwx` = Read, Write, Execute
- **Positions 5–7 (Group):** `--x` = Execute only
- **Positions 8–10 (Others):** `---` = No permissions

## Change File Permissions

In the projects directory, `project_k.txt` has write permissions for the "other" user type, while the organization's policy doesn't allow any others to have write access to any files. Using `chown o-w project_k.txt`, I removed write access for others on this file.

## Change File Permissions on a Hidden File

The file `.project_x.txt` is a hidden, archived file that should not be written to by anyone (the user and group should still be able to read it). Using `chmod u=r,g=r .project_x.txt`, permissions on this file were changed to read-only for the user and group.

## Change Directory Permissions

The files and directories in the projects directory belong to the `researcher2` user. Only `researcher2` should be allowed to access the `drafts` directory and its contents. Using `chmod g-x drafts`, I removed execute permission for the group.

## Summary

By reviewing and ensuring all users have the permissions they're authorized to have, this file permission report was completed. Least privilege is very important to ensure that only authorized people have access to data, and by modifying file permissions, that was confirmed here.

# Command Line

## Components
```bash
user@host <# or $>
# Appears only with the root user
```

## Cheatsheet
### `whoami`
- **Command**: `whoami`
- **Purpose**: The `whoami` command in Unix-like operating systems is used to display the username of the current user who is logged in to the system.
- **Usage**: Simply type `whoami` and press Enter.
- **Explanation**: 
  - This command is straightforward; it returns the username associated with the current user session. It is particularly useful in scripts, conditional access situations, or when you're operating in an environment with multiple users or switching between users.
  - `whoami` is especially useful if you've switched users within the same session using commands like `su` (switch user) or `sudo` (superuser do). It helps you confirm which user account you're currently operating under.
  - Unlike the `id` command, which can give detailed information about the user and the groups they belong to, `whoami` focuses solely on the user's identity.
  
In summary, `whoami` is a simple command to ascertain the identity of the user executing commands in the current shell session. It's a part of GNU coreutils and is available on virtually all Unix and Linux distributions.

### `su` (Switch User)
- **Command**: `su [options] [username]`
- **Purpose**: The `su` command in Unix-like operating systems is used to switch the current user context to another user. If no username is specified, it defaults to the root user.
- **Usage**:
  - To switch to the root user, simply type `su` and press Enter. You will be prompted to enter the root user's password.
  - To switch to a specific user, use `su` followed by the username, like `su username`. You'll need to enter the password for that user account.
- **Explanation**:
  - The `su` command changes the user ID and group ID of the current session to that of the specified user. It's commonly used for administrative tasks or to execute commands with the privileges of another user, most often the root user.
  - By default, `su` switches to the root user, which is the administrative user with full privileges on the system. This is a powerful tool and should be used with caution.
  - When switching users, the environment variables and the current working directory of the initial user are typically preserved. However, you can use `su -` or `su -l` to invoke a login shell, which will switch to the user's home directory and load their environment and login scripts.
  - It's important to note that `su` differs from `sudo`. While `su` switches to another user (and requires the other user's password), `sudo` executes a command with elevated privileges (and requires the current user's password, assuming they have sudo privileges).

In summary, `su` is a critical command for user management and privilege escalation in Unix and Linux systems. It allows a user to temporarily become another user, most commonly the superuser, to perform tasks requiring different permissions.

* hostname -> get the host name

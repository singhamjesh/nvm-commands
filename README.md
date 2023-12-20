# About Node Version Manager (NVM)
“nvm” stands for Node Version Manager, a tool that allows developers to manage multiple versions of Node.js on a single machine easily.

# Install a Version of NodeJS
```
nvm install <node_version>      // Install a specific version
nvm install --lts               // Install the latest LTS release
nvm install-latest-npm          // Install the latest NPM release only
```

# List Available Releases
```
nvm ls-remote
nvm ls-remote | grep -i "latest"
nvm ls-remote | grep -i "<node_version>"
```

# List Installed Versions
```
nvm ls // To display the installed Node.js versions, including the currently active version
```

# Switch to a Version
```
nvm use <node_version_or_alias>  // Switch to a specific version
nvm use --lts                    // Switch to the latest LTS version
```

# Verifying NodeJS Version
```
node -v
npm -v
nvm -v
```

# Default to a NodeJS Version (Aliasing)
```
nvm alias default <node_version>        // Sets the default version on a shell
nvm alias <alias_name> <node_version>   // Sets a user-defined alias to a versions 
nvm unalias <alias_name>                // Deletes the alias named <alias_name>
```

# Check the Path to the NodeJS Executable
```
nvm which <installed_node_version>      // Path to a specific executable
```

# Uninstall a Version of NodeJS
```
nvm uninstall <node_version>    // Uninstall a specific version
nvm uninstall --lts             // Uninstall the latest LTS release
```

# Managing global packages
```
nvm exec <version> npm install -g <package>  // To install a package globally for a specific Node.js version
nvm exec current npm list -g --depth=0   // To list all global packages for the currently active Node.js version
```

# Managing local packages
```
// To install a package locally for a specific Node.js version
nvm use <version> 
npm install <package>

// To list all local packages for the currently active Node.js version in your project directory
nvm use <version>
npm list --depth=0
```

# Additional commands
```
nvm current  // To display the currently active Node.js version
nvm alias default // To display the default Node.js version
nvm upgrade // To update “nvm” to the latest version
```


# List of commands with definition 
1. nvm alias: This command allows you to create aliases for Node.js versions. You can give a custom name to a specific Node.js version, and then use that name instead of the version number in nvm commands. For example, you can create an alias default for a specific Node.js version, and then use nvm use default to switch to that version.

2. nvm which: This command displays the path of the currently active Node.js binary, which can be useful to verify the version of Node.js that is currently being used by your system.

3. nvm reinstall-packages: This command reinstalls global npm packages from the currently active Node.js version to another version. This can be useful when you switch to a different Node.js version and want to reinstall your global npm packages for that specific version.

4. nvm migrate: This command allows you to migrate global packages from one Node.js version to another. It can be useful when you switch to a new Node.js version and want to transfer your global npm packages from the previous version to the new one.

5. nvm version: This command displays the version of nvm that is currently installed on your system, allowing you to check for updates or verify the installed version.

6. nvm deactivate: This command deactivates the currently active Node.js version, allowing you to revert to the system-installed version of Node.js or switch to a different version managed by nvm.

7. nvm exec: This command allows you to execute a command with a specific Node.js version, without permanently switching to that version. It can be useful for running a command or script with a different Node.js version than the currently active one.

8. nvm unalias: This command allows you to remove an alias that you previously created using the nvm alias command. It can be useful when you no longer need a particular alias.



# Coke - Enjoy sniffing your code

Coke is a Shell/Bash command using PHP Code Sniffer allowing per project rules management

## Configuration file

You can create a ``.coke`` file at your project root and then share it.

```
# Command used to launch PHP CodeSniffer (optional - default: phpcs)
command=phpcs
 
# Standard used by PHP CodeSniffer (required)
standard=Symfony2
 
# Verbose mode (optional - default: false)
verbose=true
 
# White list of files and directories (optional)
src/
test.php
 
# Black list of files and directories (optional)
!Tests
!src/OldFile.php
```

## Run the command

When you run the command, you can override ``.coke`` settings by passing directy configuration as argument

```
coke src test.php --standard=Symfony2 --ignore=Tests,src/OldFile.php -v
```

The order of arguments is not important

``src test.php``                   Files/Directories to include in the check
``--standard=Symfony2``            Standard to use for check
``--ignore=Tests,src/OldFile.php`` URL patterns to ignore in the check
``-v``                             Use verbose mode

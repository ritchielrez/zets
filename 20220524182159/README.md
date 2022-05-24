## How to make symlinks in Linux/BSD 

The command is:
```bash
ln -s source_file myfile
```

Here the `source_file` is the file which we're making symlinking off. And `myfile` is the symlink location.  
Beware to use here absoltue paths for both `source file` and `myfile`. Otherwise it might not work in some cases.
```bash
ln -s /home/user/opts/nvim /usr/local/bin/nvim
```

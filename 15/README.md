# Fix: quiting neovim takes time

This github issue covers this problem: https://github.com/neovim/neovim/issues/18670

Usually this problem is caused by *libuv*. Only occured when compiling ***neovim*** to `Debug` build type from source.  
Recommended to use `RelWithDebInfo` or `Release` build type. Compile ***neovim*** like with this flag to do that: 
```bash
make CMAKE_BUILD_TYPE=RelWithDebInfo
```

Better just to use stable latest ***neovim*** appimage for Linux.

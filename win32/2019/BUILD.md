
```
./vcpkg install openssl:x86-windows-static libevent[openssl]:x86-windows-static --recurse
```





-  安装 [vcpkg](https://vcpkg.io/en/getting-started.html)

- cd到  **x64_lib** 目录

- 执行安装

- 修改 Corona Simulator 程序集的编译链 （库额外包含目录）， 注意区分 x64 和 win32的配置

  

  **！！！**

  **安装库的时候可能需要代理，记得给控制台设置代理，windows10 可以直接使用clash软件启动带代理的cmd窗口**

 

```powershell
vcpkg install openssl:x64-windows-static libevent[openssl]:x64-windows-static --recurse
```


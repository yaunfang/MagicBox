# Windows使用日常记载：

- ### 查找指定端口，并关闭占用的程序。⚓

```
E:\GIT_CK\***>netstat -aon|findstr "8081"
  TCP    0.0.0.0:8081           0.0.0.0:0              LISTENING       16060
  TCP    192.168.1.32:6550      192.168.1.32:8081      ESTABLISHED     13760
  TCP    192.168.1.32:8081      192.168.1.32:6550      ESTABLISHED     16060

E:\GIT_CK\***>netstat -aon|findstr "6060"
  TCP    0.0.0.0:8081           0.0.0.0:0              LISTENING       16060
  TCP    127.0.0.1:6059         127.0.0.1:6060         ESTABLISHED     12700
  TCP    127.0.0.1:6060         127.0.0.1:6059         ESTABLISHED     12700
  TCP    192.168.1.32:8081      192.168.1.32:6550      ESTABLISHED     16060

E:\GIT_CK\***>taskkill /T /F /PID 12700
成功: 已终止 PID 11252 (属于 PID 12700 子进程)的进程。
成功: 已终止 PID 12700 (属于 PID 11332 子进程)的进程。

E:\GIT_CK\zhmp>

```

- ## FireFox（火狐浏览器）打开页面时自动切换到阅读器视图

  ☻不确定

  操作bai方法如下：

  在火狐地址栏中输入about:config,

  然后du找到zhi browser.tabs.loadBookmarksInTabs，原本是false，双击这一行，改为true就可以了。

- 
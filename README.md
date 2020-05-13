# android-dx
 Android build-tools中dx.jar的源码，版本v1.16。已修改，可以直接引入Adnroid Studio Project用来在Android上面编译dex文件。
 
## 安装
[Download Jar File](jar/dx-1.16.jar?raw=true)

## 示例
```java
        // class文件夹，或者单个class文件，或者jar
        String classFolder = "/storage/emulated/0/Android/data/com.xiaoyv.myapplication/files/build/";
        
        // 转换命令
        String[] dexCmd = new String[]{
                "--dex",
                "--verbose",
                "--no-strict",
                "--no-files",
                "--min-sdk-version=26",
                "--output=/storage/emulated/0/Android/data/com.xiaoyv.myapplication/files/dex/",
                classFolder
        };

        // 开始转换dex
        try {
            com.xiaoyv.dx.command.Main.main(dexCmd);
        } catch (Exception e) {
            e.printStackTrace();
        }
```

## 反馈
> QQEmail:1223414335@qq.com

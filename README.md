# emulestep3_3rdparty_zlib
eMule0.51d使用的第三方库zlib，本文使用版本为1.2.11，下载地址:http://zlib.net zlib是提供数据压缩用的函数库，由Jean-loup Gailly与Mark Adler所开发。
使用方法：
下载，解压缩
打开zlib-1.2.11\contrib\vstudio\vc14\vc14\zlibvc.sln,此版本解决方案中共有6个项目。重新编译zlibvc即可。
在zlibvc的项目属性页中 配置:debug->配置类型:静态库(.lib)->应用;配置:Release->配置类型:静态库(.lib)->应用。eMule0.51d的各个第三方库的引用方式不同。这一点要特别注意。
测试结果：
1.zlibvc项目编译生成之后(项目属性->配置->配置类型改为动态库(dll))，会产生dll和lib文件。凡是引用zlib的地方，都需要把这两个文件一起复制。
2.zlib.h、zconf.h是头文件，必须包含。


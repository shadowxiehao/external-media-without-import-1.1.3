# external-media-without-import-1.1.3
在大佬的插件基础下,做了小改动使该wordpress插件支持插入多个外链类型(如视频,图像等)

(原先插件介绍可见readme_old文件,或移步至https://github.com/zzxiang/external-media-without-import)

改动如下: 在下图的 MIME Type 处(先随便输入无效地址后会弹出),填入对应文件类型后再提交,前面的大小信息随便填个大于0的数就好,这样就能正确识别文件了

例如mp4视频填入: video/mp4

例如jpg图片填入: image/jpeg

![](./demonstration/demonstration0.png)

安装只要替换掉原zip 1.1.2版本包中php文件,打包上传安装替换后的版本即可(记得先卸载原版)

以插入外链视频为例:

(先随便输入无效地址后弹出下图,填写视频信息,注意类型根据你视频格式填写,这里以mp4演示, 图片同理)

![](./demonstration/demonstration1.png)

(之后便可以在媒体库找到你加入的文件了,如果信息无误的话)

![](./demonstration/demonstration2.png)


针对原版的小改动说明:将MIME Type中输入的信息记录到php文件中的'post_mime_type' => $mime_type 中的$mime_type处, 使得记录入数据库的格式信息为MIME Type中填入的格式信息

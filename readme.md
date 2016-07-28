
## 安装方法

安装

```sh
cp * ~/.config/fcitx/rime
```

然后重新部署

设置

使用fcitx-configtool 设置

 - 字体wenquanyi micro hei 
 - 字体大小16
 - 皮肤 dark 坚排选词

## 引用

rime 安装完后默认只有朙月拼音和仓颉五代，所以要使用五笔还是得动动手脚才行。实际上 Rime 默认是带五笔86和五笔拼音方案的，它们在 Rime 的共享文件夹 (/usr/share/rime-data) 里面，只要复制到其用户文件夹 (~/.config/ibus/rime) 中并且修改一下用户文件夹 (~/.config/ibus/rime)中的default.yaml 文件然后重新部署一下就行了。

将五笔86的方案文件复制到 Rime 用户文件夹中：

$sudo cp /usr/share/rime-data/wubi86.schema.yaml ~/.config/fcitx/rime（可以用文件管理器直接复制粘贴）

用文本编辑器打开 Rime 用户文件夹中的 default.yaml 文件，在 schema_list 尾部添加一行 “- schema: wubi86″，保存退出。然后重新部署一下 Rime，要重新启动一下rime. 就可以在方案菜单（F4）中选择五笔86了。

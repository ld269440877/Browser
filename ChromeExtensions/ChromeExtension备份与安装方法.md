
# Chrome Extensions 备份与恢复

从Chrome中自己抽出来，**防止作者不挂在商店里，神器就从此消失**

> 参考  
> [itgoyo/ChromePlug-in: Chrome插件备份](https://github.com/itgoyo/ChromePlug-in)  
> [备份chrome插件---重新加载备份的chrome插件](https://blog.csdn.net/enyblock/article/details/11867315)


## Chrome Extensions 备份

1. 浏览器地址栏输入:   `chrome://extensions/`  选择开发模式，单击打包扩展程序，可以看到一个“扩展程序根目录” 输入框和每个扩展程序及其ID。

<figure><center><img src="https://raw.githubusercontent.com/ld269440877/images/master/HTMLNotebook/20200121105743.png" alt="20200121105743"  title="Chrome扩展程序及其ID" width="600" height="" /><figcaption><font color=green>Chrome扩展程序及其ID</font></figcaption></center></figure>

2. 进入`C:\Users\Administrator\AppData\Local\Google\Chrome\User Data\Default\Extensions` 目录下，会看到许多以ID号命名的目录，这些文件就是插件，进入ID目录，会看到一个版本号目录。如下：
<a title="C:\Users\Administrator\AppData\Local\Google\Chrome\User Data\Default\Extensions\扩展ID\版本号">`C:\Users\Administrator\AppData\Local\Google\Chrome\User Data\Default\Extensions\apdfllckaahabafndbhieahigkjlhalf\6.3_0`</a>

3. 复制 “版本号目录全路径”到打包扩展程序_“扩展程序根目录” 里。
<figure><center><img src="https://raw.githubusercontent.com/ld269440877/images/master/HTMLNotebook/20200121110642.png" alt="20200121110642"  title="打包扩展程序_“扩展程序根目录" width="600" height="" /><figcaption><font color=green>打包扩展程序_“扩展程序根目录</font></figcaption></center></figure>

4. 在ID目录下找到对应的输出扩展程序crx和秘钥文件pem
<figure><center><img src="https://raw.githubusercontent.com/ld269440877/images/master/HTMLNotebook/20200121102456.png" alt="20200121102456"  title="扩展程序crx-秘钥文件pem" width="600" height="" /><figcaption><font color=green>扩展程序crx-秘钥文件pem</font></figcaption></center></figure>

<figure><center><img src="https://raw.githubusercontent.com/ld269440877/images/master/HTMLNotebook/20200121111205.png" alt="20200121111205"  title="扩展程序crx-秘钥文件pem路径" width="600" height="" /><figcaption><font color=green>扩展程序crx-秘钥文件pem路径</font></figcaption></center></figure>

5.  將.crx 和 .pem 两个档案移动到其他路径备份存储，例如网盘、github、Evernote
未來如果需要重新安裝擴充功能，即使已經從 Chrome 應用程式商店下架，依然可以將 .crx 檔案拖曳到 Google Chrome 瀏覽器安裝外掛功能。


## Chrome Extensions 恢复

重新载入备份的插件
1. 先将扩展程序下载保存到本地，然后将下载来的文件后缀名 `*.crx` 改成 `*.rar`，这样你就得到了一个压缩文件
2. 加载已解压的扩展程序
- 然后右键解压这个压缩文件得到一个文件夹。然后在浏览器里打开扩展程序页面（ `chrome://settings/extensions`），选中右上方开发人员模式复选框，然后再点击左上方的`加载已解压的扩展程序`按钮，选中刚刚解压出来的文件夹然后点确定即可。
- 或者直接将crx->rar解压后的文件夹拖拽到`chrome://settings/extensions`页面

<figure><center><img src="https://raw.githubusercontent.com/ld269440877/images/master/HTMLNotebook/20200121112737.png" alt="20200121112737"  title="已安装的扩展20200121" width="100%" height="100%" /><figcaption><font color=green>已安装的扩展20200121</font></figcaption></center></figure>
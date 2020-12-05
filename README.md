# open

# start xhelper
### 软件
1.操作端[X助手](https://www.pgyer.com/xhelper)(Android)

2.执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)(Windows)

3.券商软件(目前支持[同花顺](http://www.10jqka.com.cn/))(Windows)[下载地址(免费下载)](http://download.10jqka.com.cn/)


### 功能:
操作端[X助手](https://www.pgyer.com/xhelper):向N个执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)发出买股/卖股/撤销等指令

执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true):接收来自操作端[X助手](https://www.pgyer.com/xhelper)买股/卖股/撤销等指令,模拟人操作券商软件,实现自动化买卖等

### 用途
1.批量操作N个帐号

2.自动化操作股票买卖等

### 运行环境
一台Android设备和N台Windows设备

Android设备安装操作端[X助手](https://www.pgyer.com/xhelper)

Windows设备安装执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)和[同花顺](http://www.10jqka.com.cn/)

Windows设备执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)依赖环境

1.安装[Python](https://www.python.org/downloads/) #浏览器如果下载速度慢,建议使用第三方下载软件下载,安装Python时注意勾选添加环境变量

2.python -m pip install --upgrade pip  #更新pip

3.pip install websockets        #通信相关

4.pip install pyautogui         #自动化相关

5.pip install wmi pyinstaller   #设备id相关

6.pip install pyperclip         #粘贴板相关

7.pip install pandas            #数据分析相关,如有RuntimeError: The current Numpy installation ... Numpy版本问题,将numpy==1.19.4 更换成numpy==1.19.3即可 pip install numpy==1.19.3

8.pip install baidu-aip         #Baidu OCR

9.pip install pytesseract       #[Google OCR pypi](https://pypi.org/project/pytesseract/)  [Google OCR github](https://github.com/madmaze/pytesseract)

10.安装pytesseract依赖[tesseract](https://github.com/tesseract-ocr/tesseract))->[Install Tesseract via pre-built binary package](https://tesseract-ocr.github.io/tessdoc/Home.html)->[Downloads](https://tesseract-ocr.github.io/tessdoc/Downloads.html)->[UB Mannheim](https://github.com/UB-Mannheim/tesseract/wiki)->[tesseract-ocr-w64-setup-v5.0.0-alpha.20201127.exe](https://digi.bib.uni-mannheim.de/tesseract/tesseract-ocr-w64-setup-v5.0.0-alpha.20201127.exe)


注意事项:如果pip安装慢,建议在后指定[pip源](https://developer.aliyun.com/article/652884)
例如:pip install pyautogui -i https://mirrors.aliyun.com/pypi/simple/

### 执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)关联操作端[X助手](https://www.pgyer.com/xhelper)

1.执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)运行,主页面复制其客户端Id

2.操作端[X助手](https://www.pgyer.com/xhelper)-更多-设置-自动化设置-执行设备管理-右上角+ 粘贴执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)的客户端Id和其它信息保存即可，保存成功即关联完毕


### 测试
1.打开执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)

2.打开券商软件([同花顺](http://www.10jqka.com.cn/))，主页面->按F12或委托开户+委托交易->进入交易界面，注意最大化券商软件([同花顺](http://www.10jqka.com.cn/))页面,注意将买/卖操作过程中的一些确认默认勾选

3.操作端[X助手](https://www.pgyer.com/xhelper)主页面->左上角机器人图标->进行买入/卖出等测试操作,测试过程建议使用模拟账户或者非交易时间操作


### FAQ:
1.Q:执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)本地测试无响应?

  A:(1).检查是否最大化券商软件([同花顺](http://www.10jqka.com.cn/))

   (2).建议根据本地券商软件([同花顺](http://www.10jqka.com.cn/))重新将StockHelper\images\10jqka目录下无法识别的图片(sts_refresh_01.png和sts_refresh_11.png等)重新截图,然后覆盖  注意全为png图片

2.Q:同花顺如何注册模拟帐号?

  A:(1).手机下载[同花顺](http://www.10jqka.com.cn/),注册并登录[同花顺](http://www.10jqka.com.cn/),点击查看 交易->模拟,如后续在PC端登录提示用户未开户,请务必在手机上完成上述步骤

3.Q:同花顺如何重置密码?

  A:[同花顺重置密码](http://upass.10jqka.com.cn/lostpass)

4.Q:如何选择Windows设备?

  A:(1)[阿里云](http://www.aliyun.com/)Windows服务器- Windows Server  20xx 数据中心版 64位中文版(带UI)+ CPU >=4核 + 内存>=8G + 带宽(>=1M)

   (2)自备Windows主机(建议迷你主机)- CPU >=4核 + 内存>=8G + 带宽(>=1M)

   云Windows服务器与自备Windows主机优缺点对比:

   云Windows服务器 优点:(1)使用简单 (2)环境稳定 (3)随用随买 缺点:(1)按月付费 (2)部分券商禁止客户端在虚拟机(含云主机)上运行,有可能阻断运行

   自备Windows主机 优点:(1)长期使用省费用 (2)客户端交易无被阻断风险 缺点:(1)需提供单独的Windows设备,专用 (2)自行搭建支持远程登录环境 (3)需自行提供电源,网络等稳定环境

   个人建议:长期使用,使用自备Windows主机; 短期测试,使用云Windows服务器

5.Q:自备Windows主机如何支持远程登录?

  A:[花生壳](https://www.oray.com/) Windows版本安装-登录-我的应用云平台-映射模板([Windows 远程桌面](http://service.oray.com/category/153_1.html)) 创建完毕,进行诊断

   [花生壳域名诊断不同情况的处理办法](http://service.oray.com/question/5901.html)

    Q1:您的局域网服务器连接失败，请检查局域网IP与端口?

    A1:原因1:Windows版本不支持远程桌面 电脑搜索"远程桌面设置"查看确认

       解决方法:可购买密钥,升级到Windows10专业版,升级完毕,开启启用远程桌面

       电源和睡眠 屏幕 在接通电源的情况下,经过以下时间后关闭 -从不

                  睡眠 在接通电源的情况下,电脑在经过以下时间后进入睡眠状态 -从不

       原因2：未开启远程连接配置

              此电脑-属性-远程设置-远程桌面-允许远程连接到此计算机-仅允许运行使用网络级别身份验证的远程桌面的计算机连接
[花生壳+远程桌面连通家里Win7和公司Win10电脑（详细步骤）](http://service.oray.com/question/5569.html)


# end xhelper
# open

# start xhelper
###软件
1.操作端[X助手](https://www.pgyer.com/xhelper)(Android)
2.执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)(Windows)
3.券商软件(目前支持[同花顺](http://www.10jqka.com.cn/))(Windows)


###功能:
操作端[X助手](https://www.pgyer.com/xhelper):向N个执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)发出买股/卖股/撤销等指令
执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true):接收来自操作端[X助手](https://www.pgyer.com/xhelper)买股/卖股/撤销等指令,模拟人操作券商软件,实现自动化买卖等

###用途
1.批量操作N个帐号
2.自动化操作股票买卖等

###运行环境
一台Android设备和N台Windows设备
Android设备安装操作端[X助手](https://www.pgyer.com/xhelper)
Windows设备安装执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)和[同花顺](http://www.10jqka.com.cn/)

Windows设备执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)依赖环境
1.安装[Python](https://www.python.org/downloads/)
2.pip install wmi pyinstaller  #设备id相关
3.pip install pyperclip            #粘贴板相关

执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)关联操作端[X助手](https://www.pgyer.com/xhelper)
1.执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)运行,主页面复制其客户端Id
2.操作端[X助手](https://www.pgyer.com/xhelper)-更多-设置-自动化设置-执行设备管理-右上角+ 粘贴执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)的客户端Id和其它信息保存即可，保存成功即关联完毕

###测试
1.打开执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)
2.打开券商软件([同花顺](http://www.10jqka.com.cn/))，主页面->按F12或委托开户+委托交易->进入交易界面，注意最大化券商软件([同花顺](http://www.10jqka.com.cn/))页面,注意将买/卖操作过程中的一些确认
3.操作端[X助手](https://www.pgyer.com/xhelper)主页面->左上角机器人图标->进行买入/卖出等测试操作,测试过程建议使用模拟账户或者非交易时间操作

###FAQ:
1.Q:执行端[股票助手](https://github.com/handsomezhou/open/blob/master/data/StockHelper.rar?raw=true)本地测试无响应?
A:建议根据本地券商软件([同花顺](http://www.10jqka.com.cn/))重新将StockHelper\images\10jqka目录下无法识别的图片重新截图,然后覆盖

# end xhelper
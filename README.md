# 原神成就导出工具  

![GitHub](https://img.shields.io/badge/License-GPL--3.0-brightgreen?style=flat-square) ![GitHub issues](https://img.shields.io/github/issues/HolographicHat/genshin-achievement-export?label=Issues&style=flat-square) ![Downloads](https://img.shields.io/github/downloads/HolographicHat/genshin-achievement-export/total?color=brightgreen&label=Downloads&style=flat-square) ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)

- 支持导出所有成就
- 支持官服，B服与国际服
- 没有窗口大小游戏或语言等要求
- 更快、更准

## 使用说明
**打开程序前需要关闭正在运行的原神主程序**  
第一次打开需要先设置原神主程序所在路径，支持多个路径, 使用符号'*'分隔
![alt](https://upload-bbs.mihoyo.com/upload/2022/03/27/165631158/c716791daa878a473b1eb28402f5db43_1004744076428253015.png)   
### Windows7   
系统变量添加名为```NODE_SKIP_PLATFORM_CHECK```的变量并将值设为```1```   
### 自定义代理(可选)   
配置文件内添加proxy字段，详细请参看[Axios-请求配置](https://axios-http.com/zh/docs/req_config)
```json
{
  "path": [],
  "offlineResource": false,
  "customCDN": "",
  "proxy": {
    "protocol": "http",
    "host": "127.0.0.1",
    "port": 7890
  }
}
```

## 下载地址
[releases/latest](https://github.com/HolographicHat/genshin-achievement-export/releases/latest)

## 问题反馈
[issues](https://github.com/HolographicHat/genshin-achievement-export/issues)或[QQ群: 913777414](https://qm.qq.com/cgi-bin/qm/qr?k=9UGz-chQVTjZa4b82RA_A41vIcBVNpms&jump_from=webapi)

## 常见问题   
0. Q: 程序异常退出或被强行终止后，原神启动时报错: 无法连接网络(4201)   
   A: 用文本编辑器打开```C:\Windows\System32\drivers\etc\hosts```，删除```127.0.0.1 dispatch**global.yuanshen.com```后保存，重启原神   
   
1. Q: 原神启动时报错: 数据异常(31-4302)   
   A: 不要把软件和原神主程序放一起   
   
2. Q: 为什么需要管理员权限  
   A: 临时修改Hosts和启动原神  
   
3. Q: 报毒?   
   A: 执行命令或修改hosts引发，相关代码可在./utils.js,./appcenter.js下找到

4. Q: 原神进门后没有自动退出，程序输出停留在“加载完成”   
   A: 关闭Shadowsocks全局代理

5. Q: 报错 EACCES: permission denied 127.0.0.1:443   
   A: 443端口被其它程序占用，结束该进程后重试

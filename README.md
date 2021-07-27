## [我的题目](https://annna777.github.io/ctfe/)


# CTFe 使用说明

[![avatar](https://gitee.com/mmdjiji/yygq.js/raw/master/assets/license.svg)](https://choosealicense.com/licenses/gpl-3.0/) [![avatar](https://gitee.com/mmdjiji/yygq.js/raw/master/assets/language.svg)](https://www.javascript.com/) ![avatar](https://img.shields.io/badge/deploy-everywhere-blue)

本项目是一个轻量级的CTF题目展示平台。支持对flag的验证，易于部署（甚至无需服务器，在Git上即可完成部署）。

作者: [吉吉](https://github.com/mmdjiji)

## 使用Gitee Pages部署

1. 先访问 [项目GitHub地址](https://github.com/mmdjiji/ctfe) ，给项目点个Star。然后访问Gitee，再访问 [项目Gitee地址](https://gitee.com/mmdjiji/ctfe) ，点Star和Fork。这时你的仓库里就Fork了本项目。

2. 在你Fork的仓库中编辑 `problems.json` 以设置CTF题目。

3. 开启Gitee Pages服务部署以便其他人访问。

## 创建题目
一个题目对象包含如下信息(在实际配置中请删去注释)
```js
{
  "title": "",    //题目标题
  "category": "", //题目类型
  "intro": "",    //题目简介(支持html)
  "flag": ""      //题目flag的md5
}
```
`problems.json` 是由若干个题目对象组成的数组。

建议将题目的附件存放到 `files` 目录内，然后在简介中以 `<a>` 标签的形式给出下载链接。

下面给出一个题目的例子
```js
{
  "title": "签到题",
  "category": "Misc",
  "intro": "这是一道用于测试的签到题，flag{mmdjiji}",
  "flag": "98ac2c421a41a84fe1e15287ee8e93bf"
}
```

注意: 在生成题目flag的md5时，请最好使用本地生成，以防被记录后可逆。

## 不足
本项目暂不能用于计分和排行榜，仅支持本地验证。如需上述功能，请配合后端API自行实现，期待您的开源。

## 开源
本项目以 [GPLv3.0协议](https://choosealicense.com/licenses/gpl-3.0/) 开源。

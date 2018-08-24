# MyMockData
存放用于其它项目使用的mock数据，使用service woker做mock 数据的解析,参考[MockDataResolveSample](https://github.com/zj-john/MockDataResolveSample)的使用。

## 使用方式
1. fork此项目，或自建一个GitHub项目，假如项目名称为MyMockData。
2. 项目Master分支结构如下：  
```
│ README.md
│  
└─ForTest
        errorSample.json
        getSample.json
        postSample.json
```
>推荐使用一级文件夹（ForTest）作为使用mock数据的项目名使用，每个接口是一个独立的json文件

3. 开通GitHub Pages功能。  
在项目的GitHub下，选择Settings，找到GitHubPages选项，选择Master分支，开通GitHub Pages
![](/github_page.png)
此时，已经可以通过GitHub的地址访问你的json文件了，比如：  
https://zj-john.github.io/MyMockData/ForTest/getSample.json

4. 此时，你的mock data就已经配置完成。可以在需要的项目中按照[MockDataResolveSample](https://github.com/zj-john/MockDataResolveSample)的方式使用了。

Demo[地址](https://zj-john.github.io/GitHubMockServerSample/demo/public/index.html)

## Mock格式
```json
{
  "RequestMethod":["POST"],
  "ResponseHeaders":{},
  "StatusCode:": "200",
  "Response": {
    "success": true,
    "message": "",
    "data": "this is a get mock data"
  },
  "ResponseTime": 0
}
```

## 参数解析

* RequestMethod:   
Array，支持的请求方式， 例如["POST"],["POST","GET"]

* ResponseHeaders:   
Object,需要指定的返回的response header

* StatusCode:   
String/Int, 返回的状态码

* Response:  
Object, 返回的response内容

* ResponseTime:   
Int , 返回的延迟时间，单位是ms

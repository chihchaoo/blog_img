搭建博客以及使用 markdown 写作的一大痛点就是插入图片的问题。不像word或pdf，图片插入后就会跟随文档一起。markdown 中插入本地图片也是可以的，但是一旦文档或图片位置发生变化，或把文档传到博客网站上，插入的本地图片就失效了。解决方法就是把图片传到图床中，再以链接的形式插入 markdown 中。所谓图床就是一个专门用来存储图片的服务器。图床既可以自己搭建，也可以使用市面上现有的图床。最稳妥的方法当然是购买一个云硬盘然后自行搭建，但是贫穷如我，当然是没得银子去购买昂贵的云存储服务器了。免费的图床也有很多，各有优势，这里就不再赘述。目前来看，免费而又相对稳妥的解决方法就是使用 Github 了，毕竟全球最大的托管平台。


首先创建一个**公开**仓库，专门用来存放图片。依次进入 GitHub 的 "settings" -> "Developer settings" ->
"Personal access tokens"，点击 "Generate new token" 创建一个新的令牌。  
![token.png](https://cdn.nlark.com/yuque/0/2022/png/1172673/1653704441342-eda855fb-3009-43cf-a035-0566a44b704e.png#clientId=uc3da0922-ea22-4&crop=0&crop=0&crop=1&crop=1&from=ui&id=ueb93c930&margin=%5Bobject%20Object%5D&name=token.png&originHeight=525&originWidth=1379&originalType=binary&ratio=1&rotation=0&showTitle=false&size=66905&status=done&style=none&taskId=u3238fadd-e200-486b-b504-9a3d5c0f8ac&title=)
创建令牌时，有两个需要注意的地方。一是有效期 "Expiration"，我选择了时间较长的 90 天，也可以选择无期限 "No expiration"，不过 GitHub 会弹出安全提示。二是 "Select scopes" 中，网上有些教程说要全部勾选，也有的说只勾选了 "repo" 即可。我只勾选了 "repo" 发现也可以正常使用。生成令牌后注意**一定要先复制保存**，因为这个令牌只会出现一次！
![token2.png](https://cdn.nlark.com/yuque/0/2022/png/1172673/1653704953868-8fdc145c-d7cc-4fbc-9ad5-b586c1742ff9.png#clientId=uc3da0922-ea22-4&crop=0&crop=0&crop=1&crop=1&from=ui&id=ua6c02789&margin=%5Bobject%20Object%5D&name=token2.png&originHeight=364&originWidth=790&originalType=binary&ratio=1&rotation=0&showTitle=false&size=25919&status=done&style=none&taskId=u5d887eab-5272-482a-afb2-e4259062b2b&title=)
电脑上下载并安装最新稳定版本的 [PicGo](https://github.com/Molunerfinn/PicGo)。在软件中配置 Github 图床，仓库名格式：username/reponame，分支为 "main"，再把上一步生成的令牌粘贴在 Token 中就大功告成了。
![picgo.png](https://cdn.nlark.com/yuque/0/2022/png/1172673/1653705709892-eb246b99-adba-429e-9799-b91486174c2b.png#clientId=uc3da0922-ea22-4&crop=0&crop=0&crop=1&crop=1&from=ui&id=ue4188447&margin=%5Bobject%20Object%5D&name=picgo.png&originHeight=450&originWidth=800&originalType=binary&ratio=1&rotation=0&showTitle=false&size=28908&status=done&style=none&taskId=u44920ac4-fb6e-44b5-8877-2dfea3539f4&title=)


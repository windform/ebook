## 1、获取shopify API权限

### 1.1、首先要创建一个开发者的应用商店

![shopify 主题开发](/assets/2021-04-25_162045.png)  
![shopify 主题开发](/assets/2021-04-25_162211.png)

### 1.2、进入创建好的开发者应用商店，创建API专有应用

![shopify 主题开发](/assets/2021-04-25_162611.png)

### 1.3、开放主题读写权限 theme templates and theme assets，

![shopify 主题开发](/assets/2021-04-25_163152.png)

### 1.4、创建好专有应用之后，即可获得API密钥和密码。通过这些可以在开发主题时连接shopify进行实时预览和调试

![shopify主题开发](/assets/2021-04-25_163404.png)

## 2、连接shopify，下载主题到本地

### 2.1、使用以下命令行，查询主题ID。

其中密码就是创建专有应用时的密码，店铺是开发者商店的店铺名。这里要特别提醒注意的是：==**开发主题，是要在开发者应用商店下进行的**==。因此开发主题的前提是要创建一个开发者的应用商店。

```Powershell
theme get  --list -p=密码 -s=店铺.myshopify.com
```

如果报错

```Powershell
“invalid environment [development]: (invalid store domain must end in '.myshopify.com')”
```

那么在店铺域名那儿加上引号即可解决。

![shopify 主题开发](/assets/2021-04-25_173024.png)

### 3.2、下载同步主题到本地

```Powershell
theme get  -p=密码 -s=店铺.myshopify.com -t=主题id
```

![shopify 主题开发](/assets/2021-04-25_175427.png)

同步到本地的主题代码目录如下：

![shopify 主题开发](/assets/2021-04-25_175551.png)

接下来就可以正式进行主题的代码开发了。

在开发的过程中，可以执行主题监视命令**theme watch**。themtekit 会自动监听文件的变更，如果文件变更则就会自动将代码同步到 shopify 服务器

```Powershell
theme watch
```

在shopify主题预览中，可实时查看到修改后的效果。


### 安装 [chocolatey](https://chocolatey.org/install)

Windows环境下需要使用Powershell 安装，运行以下命令，完成chocolatey的安装

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

![choco安装](/assets/import.png)

安装成功后，可以使用 choco 命令测试是否安装成功

```Powershell
choco
```

![choco](/assets/import1.png)

### 使用 choco 命令安装 themtekit

```Powershell
choco install themekit
```

![安装 themekit](/assets/import3.png)

安装完成后我们可以用 theme - version 查看是否安装完成

```Powershell
theme - version
```

![theme - version](/assets/微信图片_20210425151124.png)

通过以上几个步骤，shopify的开发环境搭建完成，下面汇总一下搭建开发环境的几个命令：

```Powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

choco

choco install themekit

theme - version
```




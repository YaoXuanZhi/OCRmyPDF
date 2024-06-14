### 安装Python依赖项
```sh
conda create -n pdf_env python=3.11
# 执行这一步，会将运行ocrmypdf的第三方包都一并安装好
pip install pip install ocrmypdf
```

### 安装OCR等依赖项
```sh
# 以管理员身份运行cmd，执行以下命令：
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "[System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"

# 或者以管理员身份运行PowerShell，执行以下命令：
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

choco install --pre tesseract
choco install ghostscript
choco install pngquant
```

### 运行&调试
用vscode打开仓库根目录，F5运行调试即可
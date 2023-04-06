# 一、环境配置
前提：
硬件配置 BIOS可虚拟化  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;有WSL2
#
## 1.git
git init  
git config -global user.name  
ssh-keygen -C email@example.com  
#
## 2.git and github
下载openssh  
公钥加在github,私钥加在ssh-add  
eval "$(ssh-agent -s)"        Start-Service ssh-agent  
ssh-add  
使用 ssh -T git@github.com 命令测试 SSH 连接  
git remote add origin https://github.com/yourusername/yourrepository.git    将你在github上建立的仓库添加到本地仓库的远程  
#
## 3.容器拉起来配置编译包
sudo apt-get update  
sudo apt-get install -y build-essential  
sudo apt-get update  
sudo apt-get install -y gdb  
#
## 4.安装必要插件
C/C++  
docker  
dev containers  
remote explorer  
wsl  
#
## 5.https转ssh
git remote set-url origin git@github.com:jianmosier/AlgorithmLearning.git  
git config --global --add safe.directory /com.docker.devenvironments.code  当提示文件夹不安全时可以用这个

ssh-keygen -t ed25519 -C "your_email@example.com"  
eval "$(ssh-agent -s)"  
ssh-add ~/.ssh/id_ed25519  
ssh -T git@github.com




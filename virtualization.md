# Virtualization related

## vagrant

```shell
# vagrant box
vagrant box list
vagrant box add <Box name> <Download url or box file> # Decide OS
vagrant box remove
# 初始化 Box，產生 Vagrantfile
vagrant init
# 開機
vagrant up
# 休眠
vagrant suspend
# 取消休眠
vagrant resume
# 關機
vagrant halt
# 重新開機
vagrant reload
# 以完整的配置開機
vagrant provision
# ssh 到虛擬主機
vagrant ssh
vagrant ssh-config
# 停止虛擬機運作並銷毀所有資源
vagrant destroy
# 環境打包
vagrant package
# 看狀態
vagrant status
vagrant global-status
```

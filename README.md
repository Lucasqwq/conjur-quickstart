# conjur-test

*sudo apt-get install cpu-checker

*kvm-ok

*sudo usermod -aG kvm $USER #把kvm功能加入user

*groups

*exit

*sudo shutdown -r +1(重開)

*sudo apt install gnome-terminal

*sudo apt-get update

*sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

*sudo mkdir -p /etc/apt/keyrings

*curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

*echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

*sudo apt-get update
 
*sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

*sudo docker run hello-world

*sudo apt-get update

*sudo apt-get install ./docker-desktop-<version>-<arch>.deb

*systemctl --user start docker-desktop ###不可sudo,僅可使用當期使用者
 
*docker compose version
---------------------------------------------------quickstart------------------------------------------------------------------------------------
虛擬機重啟的話 container要全關掉再重新創建

*docker-compose down

*docker-compose up -d



取得container的CLI
*docker-compose exec client




重新創造一個admin的key

*docker-compose exec conjur conjurctl account create myConjurAccount > admin_data




再連接到conjur client

*docker-compose exec client conjur init -u conjur -a myConjurAccount




這樣就可以以admin登入

*docker-compose exec client conjur authn login -u admin




就可以load policy 記得把要寫入的policy.yml檔案 丟進conf/policy

*docker-compose exec client conjur policy load --replace root policy/conjur.yml > my_app_data_2

(version 會改變)






—--------------------------------------------------do it myself above---------------------------------------------------






*egrep "vmx|svm" /proc/cpuinfo

*sudo apt-get install cpu-checker

*kvm-ok

*sudo apt-get install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virtinst virt-manager

*sudo systemctl is-active libvirtd

*whoami

*sudo usermod -aG libvirt $USER

*sudo usermod -aG kvm $USER #把kvm功能加入user

*groups

*exit

*sudo shutdown -r +1

*sudo apt install gnome-terminal

*sudo apt-get update

*sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
 
*sudo mkdir -p /etc/apt/keyrings

*curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

*echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

*sudo apt-get update
 
*sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

*apt-cache madison docker-ce

*sudo docker run hello-world

*sudo apt-get update

*sudo apt-get install ./docker-desktop-<version>-<arch>.deb

*systemctl --user start docker-desktop ###不可sudo,僅可使用當期使用者
 
*docker compose version

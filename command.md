#ping_test
ping -c 5 10.0.2.226

#배스천호스트에서의SSH접속
chmod 600 my-key.pem
ssh -i my-key.pem ec2-user@10.0.2.150

ping –c 5 8.8.8.8 #Fail_프라이빗서브넷의_자원이므로
exit

#NAT_gateway_외부_접속_테스트
chmod 600 my-key.pem
ssh -i my-key.pem ec2-user@10.0.2.150

ping –c 5 8.8.8.8

#웹만들기
sudo dnf update –y
sudo dnf install –y git stress nginx #git,stress,nginx_설치

sudo systemctl start nginx
sudo systemctl enable nginx
systemctl status nginx --no-pager

mkdir ~/project #웹서버_구성을_위한_파일_다운로드_및_재배치
git clone https://github.com/my-ciel/aws-web.git ~/project
sudo cp –r ~/project/* /usr/share/nginx/html/
sudo ls /usr/share/nginx/html/

sudo cp -f /usr/share/nginx/html/index1.html /usr/share/nginx/html/index.html

#부하테스트_(stress_설치_및_부하_주기)
sudo -i
stress --version

yum -y install stress #설치정보확인
stress --version

stress --cpu 4 --timeout 600 #cpu를_400%_사용하는_부하를_600초동안_테스트
  

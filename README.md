# AWS_cloud_study
-AWS cloud
  리전 : 지리적 영역. 보통은 국가 단위이며 2개 이상의 가용영역(AZ)로 구성됨
   리전 선택시 주의사항 : 
   1) 데이터 거버넌스, 법적 요구 사항
   2) 고객에 대한 근접성 (지연시간)
   3) 리전 내에서 사용 가능한 서비스
   4) 비용
  가용영역(Zone) : AWS 인프라의 완전히 격리된 파티션 (=데이터 센터)
  PoP : 트래픽 허브 역할을 하는 물리적 데이터 센터

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e49ed6e4-66bc-4a9f-8855-307eb9c83a3b" />


-EC2 : AWS에서 제공하는 가상 서버 서비스

-VPC(Virtual Private Cloud) : 가상 네트워크 

-Subnet : VPC를 분할하는 IP 주소의 범위이며, 퍼블릭 또는 프라이빗으로 분류.

-Internet Gateway : VPC를 인터넷과 연결하는 게이트웨이

-NAT Gateway : 프라이빗 서브넷을 인터넷에 연결하는 게이트. 프라이빗 인스턴스가 인터넷에서 인바운드 연결 요청을 수신하지 못하도록 차단. (아웃바운드만 가능)

-Security Group : EC2 인스턴스의 가상 방화벽

-SSH : 원격으로 EC2에 안전하게 접속하기 위한 프로토콜
<img width="1136" height="1020" alt="스크린샷 2026-06-24 165719" src="https://github.com/user-attachments/assets/e629242e-2b89-4add-a94c-56d1afed145f" />

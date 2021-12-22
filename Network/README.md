<div align='center'>
  <h1>Network</h1>
</div>


**Contents**
- [- Subnet](#--subnet)
- [IP Address](#ip-address)
- [Network/Broadcast Address](#networkbroadcast-address)
- [Subnet](#subnet)
---
## IP Address
- IP 주소는 네트워크의 규모에 따라 A ~ E 클래스로 나누어져 있으며 일반적으로 A ~ C클래스를 사용한다.
- 네트워크 크기에 따라 32비트의 IP 주소를 네트워크 ID와 호스트 ID로 bit를 조정하여 IP 주소를 A ~ E클래스로 구분할 수 있다.

<div align='center'>
    <img style="margin: 30px 0; width: 500px" src='./ip_1.jpg'>
</div>


- A 클래스는 8비트의 네트워크 ID와 24비트의 호스트 ID로 구성된다.
- A 클래스의 1옥텟(8비트)의 범위는 2진수로 00000001 ~ 01111111이며 10진수로 변환하면 1~127이다. 2~4 옥텟의 범위는 0 ~ 255의 범위를 가지고 전체 범위는 1.0.0.0 ~ 127.255.255.255 이다. 


- B 클래스의 1 옥텟의 범위는 2진수로 10000000 ~ 10111111이고, 10진수로 변환하면 128 ~ 191이 된다. 전체 범위는 128.0.0.0 ~ 191.255.255.255가 된다.

- C 클래스의 1옥텟의 범위는 2진수로 11000000 ~ 11011111이며, 10진수로 변환하면 192~223이다. 192.0.0.0 ~ 223.255.255.255의 범위를 가진다.

<div align='center'>
<img style="margin: 30px 0; width: 500px" src='./ip_2.jpg'>
</div>

- 사설 IP 주소는 공인 IP주소로 사용할 수 없다.
- cmd에서 `ipconfig` 명령어를 실행해서 IP 주소를 확인할 수 있다.

---
## Network/Broadcast Address



- 네트워크와 브로드캐스트 주소로 컴퓨터나 라우터가 자신의 IP로 사용하면 안된다.
<div align='center'>
    <img style="margin: 30px 0; width: 500px" src='./ip_3.jpg'>
</div>
- 네트워크 주소는 호스트 ID가 10진수로 0, 2진수 00000000인 주소이다. 

- 네트워크 주소는 전체 네트워크에서 작은 네트워크를 식별하는데 사용되고 호스트 ID가 10진수로 0이면 그 네트워크 전체를 대표하는 주소가 된다. 

- 예를들어 192.168.1.0은 네트워크 192.168.1.1 ~ 6의 IP 주소를 대표하는 네트워크 주소이다. 
<div align='center'>
<img style="margin: 30px 0; width: 500px" src='./ip_4.jpg'>
</div>

- 브로드캐스트 주소는 호스트 ID가 10진수로 255고 2진수로 11111111인 주소이다.

- 브로드캐스트 주소는 네트워크에 있는 컴퓨터나 장비 모두에게 한 번에 데이터를 전송하는데 사용되는 전용 IP 주소이다.
- 전체 네트워크에 데이터를 전송하려면 호스트 ID에 255를 설정하면 된다.
- 192.168.1.255의 브로드 캐스트로 데이터를 전송하면 네트워크 안에 있는 모든 컴퓨터가 데이터를 전달 받게 된다.
- 네트워크 주소와 브로드캐스트 주소는 컴퓨터에 설정할 수 없다.


---
## Subnet
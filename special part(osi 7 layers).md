
## OSI 7 계층

**[what is osi 7 layers?]**

osi 7계층은 7단계로 규격화 된 (네트워크 장비의 데이터 송수신 과정)이다. 

**[왜 나누었을까?]**

- 송수신 과정에서 벌어지는 문제에 대한 명확한 진단이 가능하다.
- 데이터의 흐름을 한눈에 볼 수 있다.

**[7계층에 대한 비유적 설명]**

1.7-layer(application_layer) -> 내가 편지에 전달할 내용을 적는다 - 사용자가 자신의 pc상에 존재하는 어플리케이션에 다른 네트워크 기기의 어플리케이션에 전달할 데이터를 입력한다

편지-application

전달할 내용 - data

2.6-layer(presentation_layer) -> 편지를 받을 수신자를 고려하여 편지 내용이 표준화된 형식으로 표현된다(one,two,three,four)->(1,2,3,4)  -  7계층에서 만들어진 데이터가 다른 네트워크
edge가 식별할 수 있도록 표준화된 형태로 encoding되고, 이후 데이터에 대한 보안이 요구된다면, 그 데이터의 형태를 조작되어 암호화된다.


3.5-layer(session-layer) -> 두 네트워크간 데이터가 이동하는 회선의 생성,유지,종료등이 결정된다.

ex)1.쌍방연결, 2.일방연결

4.4-layer(transport-layer) -> 편지에 수신자가 사는 아파트내 위치가 결정된다. 경우에 따라 편지의 송신위치가 결정될 수도 있다. ex)from 499 to 9  - 수신자 측 어플리케이션의 포트번호가 결정되고, 경우에 따라 송신자 측 어플리케이션의 포트번호가 결정될 수도 있다. 

아파트 - 네트워크 edge

아파트 내 가정집의 호수 - port_number

what is port?
https://en.wikipedia.org/wiki/Port_(computer_networking)

5.3-layer(network-layer) -> 편지가 수신될 위치와 송신될 위치의 지도상 위치와 편지가 이동할 경로가 결정된다 - 인터넷상에서 수신지와 송신지들을 구별해주는 번호가 결정된다. 또한 데이터가 이동할 경로가 결정되기도 한다.

6.2-layer(data-link-layer) -> 데이터가 전달될 수신지를 포함한 lan내에서 데이터가 어떻게 전달될지 결정된다

7.2-layer에서 결정된 내용에 따라 데이터가 물리적으로 회선을 따라 이동하거나(데이터가 수신되거나 송신된다) 증폭되거나 변형된다.
->원문:Within the semantics of the OSI model, the physical layer translates logical communications requests from the data link layer into hardware-specific operations to cause transmission or reception of electronic (or other) signals.[4][5] The physical layer supports higher layers responsible for generation of logical data packets

**[각 계층에서 수행되는 작업]**

#### 송신과 수신시 통신 절차

![img](https://insights.profitap.com/hs-fs/hubfs/The%207%20Layers%20of%20OSI.png?width=840&name=The%207%20Layers%20of%20OSI.png)

#### 계층의 분류 

1.상위 계층과 하위 계층


#### 각 계층에서 동작하는 장비와 각 계층별 통신규약

![img](http://linux-training.be/networking/images/networklayers.png) 

각 계층에서 장비들이 정해진 통신규약(프로토콜)을 따라 동작하므로써 데이터가 아래 절차대로 가공되어, 우리가 원할한 송신과 수신을 할 수 있게 된다.

#### 계층의 흐름에 따른 데이터의 변화

![img](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/what-is-data-encapsulation-in-networking-process-148532037a490a19.jpg)
![img](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/what-is-data-encapsulation-in-networking-intro-651bf3770350727c.jpg) ![img](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/what-is-data-encapsulation-in-networking-encapsulated-data-term-a781975b6bcfd332.jpg)











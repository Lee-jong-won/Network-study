
# 네트워크 공부 정리 내용 

후니의 시스코 네트워킹(https://smartstore.naver.com/bookmount/products/4661023484?NaPm=ct%3Dklj50hfs%7Cci%3D80f5b7579df8cdcd01964caad5866d76b0f4a041%7Ctr%3Dsls%7Csn%3D246606%7Chk%3Da9f29bca4d45dd6aabd77239762586265ba35bd5)를 읽고 part1, part2(14~57)부분을 정리했습니다.

## 네트워킹과 네트워크의 정의

1.장비들끼리 서로 유무선으로 연결되있다.

2.서로 데이터를 주고 받는다.

->통신장비들이 1,2를 모두 만족하는 것은 장비들이 서로 네트워킹을 한다는 것을 의미하고, 서로 네트워킹하는 장비들의 집합을 네트워크라고 한다.

## 네트워크의 종류

1.인터넷(INTERNET):인터넷은 어원적으로(INTER:상호)+(NET:그물)로 분석된다. 직역하면 함께 쓰는 그물로 해석되고, 컴퓨터 공학적으로는 무수히 많은 소규모 네트워크들이 모여 만들어진 거대한 네트워크로 해석됩니다.

2.인트라넷(INTRANET):인트라넷은 어원적으로(INTRA:안에)+(NET:그물)로 분석된다. 직역하면 내부 에서만 쓰는 그물로 해석되고, 컴퓨터 공학적으로는 인터넷과 분리된 독립적인 네트워크를 의미한다.

## LAN VS WAN (네트워크가 지원하는 통신거리에 따른 분류)

- 네트워크가 지원하는 통신를 기준으로 나눈 네트워크의 종류

![img](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6e/Data_Networks_classification_by_spatial_scope.svg/375px-Data_Networks_classification_by_spatial_scope.svg.png)

LAN:LOCAL AREA NETWORK의 약자로, 비교적 좁은 범위(학교,연구소,사무실)에서 통신을 지원하는 네트워크를 말한다.

WAN:WIDE AREA NETWORK의 약자로, 비교적 넓은 범위(대륙간 통신)에서 통신을 지원하는 네트워크를 말한다.

## LAN의 종류 대표적인 2가지

### 1.Ethernet:LAN을 구성하는 장비들이 서로 CSMA/CD 방식으로 통신하는 LAN

#### csma/cd란 무엇일까?

csma/cd는 lan에서 장비들간의 통신 규약 중 하나이다(규약이란 말이 처음에 어렵게 느껴질 수 있으니, 처음엔 일단 규약=약속으로 받아들여도 좋다). 하지만 이것이 csma/cd에대한 엄밀한 설명은 아니다. 엄밀히 이 용어를 정의하자면, csma/cd란 아래 절차를 따르는 lan 내부 장비간 통신규약이다.
통신규약 즉 프로토콜이란 네트워크 장비간 통신의 효율성,보안성,편리성을 위해 네트워크 내 통신 장비 사이에 정의된 통신규칙을 의미한다. 통신규약은 format(데이터를 어떤 형태로 보낼 것인지),
semantic(데이터를 어떻게 보낼 것인지), time(데이터를 어떤 순서로 혹은 어떤 속도로 보낼것인지) 와 같이 3요소로 정의된다.

통신규약에 포함될 수 있는 내용)

방식 -> 기대효과,side effect
기대효과 대비 side effect큰 통신규약은 수정되어 더 나은 통신 규약이 개발되기도 한다.

1.데이터 흐름 제어법 
2.데이터 단편화 방식,데이터 재조립 방식
3.두 통신 기기간 연결 제어 방식
4.흐름 제어 방식
5.주소 지정 방식
6.다중화 방식
->한정된 회선을 여러 통신기기들이 어떻게 이용할 것인지에 대한 규약




![img](https://upload.wikimedia.org/wikipedia/commons/thumb/3/37/CSMACD-Algorithm.svg/660px-CSMACD-Algorithm.svg.png)

통신 규약에 대한 자세한 설명(아래 순서를 따라 데이터가 한 host(송신 네트워크 장비)에서 다른 host(수신 네트워크 장비)로 전송된다.)

#### Step1:Carrier sense

1.송신 측이 lan 내부 회선에 데이터 송신이 이루어지고 있는지 확인한다.

2.회선에 송신이 감지되지 않으면, 송신을 개시한다(감지되면, 개시하지 않는다.)

#### Step2:Collision Detection

- 송신 측이 보낸 데이터가 다른 node들로부터 전송된 데이터와 충돌이 일어나는지 확인한다.

1. 송신 측이 보낸 데이터가 다른 node로부터 전송된 데이터와 충돌이 감지되지 않으면, 송신이 완료된다.

2. 송신 측이 보낸 데이터가 다른 node로부터 전송된 데이터와 충돌이 감지되면, step3->step4순으로 데이터 전송 절차가 진행된다.

#### Step3:Jam signal transmist
 
- 송신 측이 데이터를 전송하는 동안 다른 node들이 데이터를 전송하지 않도록, 송신 측이 LAN상의 모든 node들에 broadcast(LAN상의 모든 node들에 전달되는 신호)신호인 jam signal을 보낸다.

- Jam signal은 48bit 신호이다.

#### Step4:Waiting for back off time

1. 충돌이 발생하고 jam signal을 보낸 이후에, 송신측은 random한 시간동안 대기한 이후. 다시 데이터를 목적지로 보내고 동시에 시도 변수 attempt를 1 증가시킨다(송신측이 대기하는 이 시간은 backoff-time이라고 불린다)

2. 이후, 송신이 완료될 때까지 step1~step3를 다시 반복한다(다만, 미리 설정된 한계시도횟수(maxattempt)와 attempt 변수에 저장된 횟수의 크기가 같아지면, 송신 측은 송신이 불가능하다고 판단하고 송신을 중단한다.) 

### 2.TOKEN ring network:lan을 구성하는 장비들이 token ring이라는 회선을 이용해 통신하는 lan

- 토큰링을 회선을 이용한 lan의 모습 

![img](https://www.cse.iitk.ac.in/users/dheeraj/cs425/fig.lec07/ring.gif)

#### token ring 네트워크에서 통신 규약

1.token이 일정한 간격을 두고, lan 내부 컴퓨터들로 수시로 옮겨다닌다.

2.local에 있는 node가 token을 가지고 있는 동안, 그 node는 데이터를 송신할 수 있고, token을 가지지 않고 있는 node들은 데이터를 송신할 수 없다.

--->ethernet과 구분되는 점은 데이터 전송 시 collision이 발생하지 않는 다는 것이다.

## LOCAL LAN 에서 NETWORK EDGE(host) 사이에서 벌어지는 통신의 종류

1.unicast:LAN에 있는 한 edge가 다른 하나의 edge에 데이터를 전송하는 것
 
2.broadcast:Lan에 있는 한 edge가 lan 전체에 데이터를 전송하는 것
 
3.multicast:LAN에 있는 한 edge가 lan 상의 모든 컴퓨터에 데이터를 전달하는 것이 아니라, 한 개 이상의 컴퓨터들에 데이터를 전송하는 것.

![img](https://forum.huawei.com/huaweiconnect/data/attachment/forum/201911/20/150616may2y00y2l0yly0q.png) 




## OSI 7 계층

**[what is osi 7 layers?]**

osi 7계층은 7단계로 규격화 된 (네트워크 장비의 데이터 송수신 과정)이다. 

**[왜 나누었을까?]**

- 송수신 과정에서 벌어지는 문제에 대한 명확한 진단이 가능하다.
- 데이터의 흐름을 한눈에 볼 수 있다.

**[osi 7 계층 모델을 참조한 데이터 송수신 과정]**

![img](https://insights.profitap.com/hs-fs/hubfs/The%207%20Layers%20of%20OSI.png?width=840&name=The%207%20Layers%20of%20OSI.png)

**[각 layer에서 데이터 송수신에 관여하는 장비들의 동작]**

![img](http://files.itworld.co.kr/archive/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202016-06-02%20%EC%98%A4%ED%9B%84%202_56_08(1).jpg)







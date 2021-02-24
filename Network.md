
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

- csma/cd란 무엇일까?

csma/cd는 lan에서 장비들간의 통신 규약 중 하나이다(규약이란 말이 처음에 어렵게 느껴질 수 있으니, 처음엔 일단 규약=약속으로 받아들여도 좋다). 하지만 이것이 csma/cd에대한 엄밀한 설명은 아니다. 엄밀히 이 용어를 정의하자면, csma/cd란 아래 절차를 따르는 lan 내부 장비간 통신규약이다.

![img](https://upload.wikimedia.org/wikipedia/commons/thumb/3/37/CSMACD-Algorithm.svg/660px-CSMACD-Algorithm.svg.png)

통신 규약에 대한 자세한 설명(아래 순서를 따라 데이터가 한 host(송신 네트워크 장비)에서 다른 host(수신 네트워크 장비)로 전송된다.)

1.lan 내부에 데이터 송수신이 이루어지고 있는지 확인한다.
2-1.이루어 지고 있다면, 


### 2.TOKEN ring network:lan을 구성하는 장비들이 token ring이라는 회선을 이용해 통신하는 lan













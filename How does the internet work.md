

# 인터넷은 어떻게 동작하는가?

***인터넷*** 은 웹의 핵심적인 기술입니다. 인터넷의 가장 기본적인 것은, 컴퓨터들이 서로 통신 가능한 거대한 네트워크라는 것입니다.


## 단순한 네트워크
두 개의 컴퓨터가 통신이 필요할 때, 우리는 다른 컴퓨터와 물리적으로 (보통 이더넷 케이블) 또는 무선으로 (예를 들어, WIFI 나 Bluetooth) 연결되어야 합니다. 모든 현대 컴퓨터들은 이러한 연결 중 하나를 이용하여 연결을 지속할 수 있습니다.

![1:1 연결](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work/internet-schema-1.png)

이러한 네트워크는 두 대의 컴퓨터로 제한되지 않습니다. 원하는 만큼의 컴퓨터를 연결할 수 있습니다. 그러나 이렇게 연결할 수록 매우 복잡해집니다. 예를 들어 10대의 컴퓨터, 100대의 컴퓨터를 연결하려면 무수히 많은 케이블이 필요합니다.

![너무많은케이블](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work/internet-schema-2.png)

이 문제를 해결하기 위해 네트워크의 각 컴퓨터들은 ***라우터*** 라고하는 소형 컴퓨터에 연결합니다. 이 라우터에는 단 하나의 작업만을 수행합니다. 바로 연결된 컴퓨터끼리의 최적의 경로를 찾아주며 잘 통신할 수 있도록 하는것 입니다.

이 라우터를 시스템이 추가한다면 n대의 컴퓨터 네트워크에는 n개의 케이블만이 필요하게 됩니다.

![라우터](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work/internet-schema-3.png)

## 네트워크 속의 네트워크

아직까지의 소형 네트워크에서는 잘되었습니다. 하지만 수백, 수천, 수십억 ... 대의 컴퓨터를 연결하는 것은 어떨까요? 문론 단일 라우터는 그 정도까지 확장할 수는 없지만 라우터 또한 라우터와 연결할 수 있으며, 무한히 연결할 수 있습니다.

![무한라우터](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work/internet-schema-5.png)

이러한 네트워크는 인터넷이라고 부르는 것에 가깝지만, 이더넷 케이블로 전 세계의 컴퓨터들을 연결하는 것은 분명 한계가 있습니다. 이 문제를 해결하기위하여 이미 집마다 연결되어있는 전력 및 전화 케이블이 있습니다. 전화기 기반의 시설은 이미 전 세계 어느 곳과도 연결되어 있으므로 우리가 필요로 하는 완벽한 배선이라고 할 수 있습니다. 따라서 네트워크를 전화 시설과 연결하기 위해서는 ***모뎀*** 이라는 특수 장비가 필요합니다. 이 모뎀은 우리 넽워크의 정보를 전화 시설에서 처리할 수 있는 정보로 바꾸며, 그 반대의 경우도 마찬가지 입니다.

![모뎀](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work/internet-schema-6.png)

이렇게 모뎀을 통하여 네트워크에 연결하게 됩니다. 다음 단게는 네트워크에서 도달하려는 메세지를 보내는 것입니다. 이를 위해 네트워크를 인터넷 서비스 제공 업체(Internet Service Provider, ISP)에 연결합니다. ISP는 모두 함께 연결되는 몇몇 특수한 하우터를 관리하고 다른 ISP의 라우터에도 엑세스 할 수 있는 회사입니다. 따라서 네트워크 메세지는 ISP 네트워크의 네트워크를 통하여 목적지 네트워크로 전달됩니다. 인터넷은 이러한 전체 네트워크 인프라로 구성됩니다.

![ISP](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work/internet-schema-7.png)

## 컴퓨터 찾기


컴퓨터에 메세지를 보내려면 메세지를 받을 특정 컴퓨터를 지정해야합니다. 따라서 네트워크에 연결된 모든 컴퓨터에는 IP(Internet Protocol) 주소라는 고유한 주소로 연결되어야 하며, 이 주소는 점『』으로 구분한 네 개의 필드로 존재합니다. ex: ```192.168.0.1```

컴퓨터는 이러한 주소로 다른 컴퓨터를 찾아가지만, 인터넷 사용자들은 이 숫자들을 외우기 쉽지 않을 것 입니다. 그래서 사용자들은 ***도메인 이름*** 이라고하는 읽을 수 있는 문자로 접근할 수 있습니다. 주소를 도메인 이름으로 변경해주는 서비스를 (DNS, Domain Name Service)라고 합니다.

![DNS](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work/dns-ip.png)

## 인터넷과 웹


웹 브라우저를 사용하여 웹을 탐색 할 때 일반적으로 도메인 이름을 사용하여 웹 사이트에 접속합니다. 그렇다면 인터넷과 웹은 같은 의미를 나타내는 것 일까요? 그렇게보이지만 생각보다 단순하지 않습니다. 앞에서 보았듯이 인터넷은 수십억 대의 컴퓨터를 모두 연결하는 기술 인프라입니다. 이러한 컴퓨터들 중에 일부는 ***웹 서버*** 로서 웹 브라우저가 이해할 수 있는 서비스를 제공합니다. 인터넷은 인프라이며 웹은 그 인프라 기반 위에 구축된 서비스의 일종입니다. 웹 뿐만 아니라 인터넷 위에 구축된 다른 서비스들(이메일 등)도 있을 알아야 합니다.



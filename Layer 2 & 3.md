## Data link layer & Network layer

### - APR란?
+ 3계층의 network layer 프로토콜 중 하나이다. ARP는 주로 2계층의 주소를 알아내는 것이다. 반대로 2계층 주소정보를 이용해서 3계층 주소를 알아내는 RARP라는 것도 있다.
이러한 특성으로 2.5계층쯤에 있다고 말하기도 한다. 

### - Internet에서 데이터 단위는?
+ 각 계층마다 불리는 데이터 단위의 이름은 다 다르다. 응용계층은 user data, 전송계층은 segment, 네트워크 계층은 Datagram이나 packet, 
데이터링크와 물리계층은 Frame 이라고 한다. 이때 전송계층, 네트워크 계층, 데이터링크 계층, 물리계층은 합해서 packet이라고도 한다. 

### - data link 와 network layer에서의 주소체계
+ 3계층은 주소의 값이 노드의 위치를 어느정도 알 수 있어야하므로, MSB bit에 네트워크 내에서 물리적으로 할당되는 특징과 2계층은 그런 특징이 없다는 것처럼 각 계층별로 주소의 역할이 다르기 때문에 주소체계가 다 다르다. 2계층은 NIC에서 임의로 할당하고, 3계층은 IANA에서 할당하며, 인터페이스의 물리적인 위치에 따라 계속 할당한다.

### - 2계층 주소의 notation
+ 2계층의 주소는 6바이트로 이루어져 있다. hexadecimal notation으로 되어 있어 16진수로 표현하고 : 으로 구분짓는다. 6바이트중 앞의 3바이트는 NIC에서 부여받은 고유의 번호 즉, 식별번호이다. 이것을 OUI라고 한다. 

### - 2계층 주소 LSB
+ destination 48bit(6byte)중에 LSB bit의 값에 따라 multicast, unicast로 나눌 수 있다.
unicast address는 목적지가 하나인 것을 나타내고 LSB bit가 0일때이다.
multicast address는 목적지가 여러개인 것을 나타내고 1일때이다.
Broadcast address는 6byte가 모두 F일때를 나타내며 모든 노드가 목적지임을 나타낸다.



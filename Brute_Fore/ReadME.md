Brute Force 공격을 탐지하는 snort rule(DVWA 이용)

패킷전송 : 
![image](https://user-images.githubusercontent.com/52124043/61123249-d7b26b00-a4de-11e9-9cfa-10c65394a586.png)

GET방식으로 username과 password가 url에 그대로 나타나 전송되는것을 알 수 있다.
그러므로 username과 password 부분에 brute force 공격으로 아이디와 비밀번호를 유추할 수 있을 것이다.

burp suite로 brute force 공격을 시도
![image](https://user-images.githubusercontent.com/52124043/61125995-43e49d00-a4e6-11e9-8aab-99d58f998b68.png)

결과 : 
![image](https://user-images.githubusercontent.com/52124043/61126104-8ad29280-a4e6-11e9-8fab-b2d3f315b67c.png)

snort rule : alert tcp any any -> any any (msg:"BRUTE_FORCE_ATTACK"; content:"username"; nocase; content:"password"; nocase; threshold:type both, track by_src, count 10, seconds 20; sid:111111;)



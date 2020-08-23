XSS-alert 함수 이용 공격 방지 snort rule(Dvwa 이용)

![image](https://user-images.githubusercontent.com/52124043/61203879-9dd3a580-a726-11e9-9d2a-9d849edeb095.png)

URL의 nmae 인자 값으로 스크립트 삽입시 실행된다.

snort rule : alert tcp any any -> any any (msg:"XSS_alert Attack!"; content:"script"; nocase; content:"alert("; nocase; sid:5555;)

![image](https://user-images.githubusercontent.com/52124043/61435915-96094080-a974-11e9-9746-eaa402662d68.png)

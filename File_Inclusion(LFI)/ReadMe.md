LFI 공격 탐지 snort rule (DVWA 이용)

URL의 page인자로 파일명이 전달

![image](https://user-images.githubusercontent.com/52124043/61355286-03529e00-a8af-11e9-9847-3a67cbd728b0.png)

리눅스 기본경로 접근을 snort rule로 탐지(=/etc)

![image](https://user-images.githubusercontent.com/52124043/61432930-e8466380-a96c-11e9-8de5-3729b758851a.png)

snort rule : 

alert tcp any any -> any any (msg:"LFI_Attack!"; content:"GET /"; nocase; content:"=/etc"; nocase; sid:3434;)

RFI 공격 탐지 snort rule(DVWA 이용)

URL의 인자를 이용해 외부 서버의 파일에 접근

![image](https://user-images.githubusercontent.com/52124043/61355916-46614100-a8b0-11e9-8eca-9a4b1fa17b9a.png)

snort rule을 이용해 =http와 =https를 탐지

![image](https://user-images.githubusercontent.com/52124043/61432755-53dc0100-a96c-11e9-8749-3a9199928c79.png)


snort rule : 

alert tcp any any -> any any (msg:"RFI_Attack!"; content:"GET /"; nocase; pcre:"/(=http|=https)/i"; sid:67;)

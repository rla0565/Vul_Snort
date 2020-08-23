Web_shell을 이용한 공격 탐지 snort rule(Dvwa, weevely 이용)

weevely를 이용해 web_shell을 만들어 DVWA에 File upload

![image](https://user-images.githubusercontent.com/52124043/61441698-2483bf00-a981-11e9-8988-13b4e5ed9406.png)

ASP web shell(CreateObject함수) 탐지 snort rule

alert tcp any any -> any any (msg:"Web_shell_Upload_ASP_CreateObject_func_Attack!"; content:"|0d 0a 0d 0a|<%"; nocase; content:"CreateObject("; nocase; sid:75657;)

![image](https://user-images.githubusercontent.com/52124043/61518005-93295100-aa43-11e9-904f-61878763c58c.png)



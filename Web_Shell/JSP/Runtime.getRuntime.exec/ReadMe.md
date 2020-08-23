Web_shell을 이용한 공격 탐지 snort rule(Dvwa, weevely 이용)

weevely를 이용해 web_shell을 만들어 DVWA에 File upload

![image](https://user-images.githubusercontent.com/52124043/61441187-0d909d00-a980-11e9-951c-35c6374839e9.png)

JSP web shell(Runtime.getRuntime().exec함수) 탐지 snort rule

alert tcp any any -> any any (msg:"web_shell_Upload_jsp_Runtime.getRuntime_func_Attack!"; content:"|0d 0a 0d 0a|<%"; nocase; content:"Runtime.getRuntime"; nocase; sid: 213124;)

![image](https://user-images.githubusercontent.com/52124043/61517932-5eb59500-aa43-11e9-83b8-7f03699f84ae.png)



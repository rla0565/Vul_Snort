Web_shell을 이용한 공격 탐지 snort rule(DVWA, weevely 이용)

weevely를 이용해 web_shell을 만들어 DVWA에 File upload

![image](https://user-images.githubusercontent.com/52124043/61447801-a88f7400-a98c-11e9-876c-42cf7fb9e951.png)

php web shell(passthru함수) 탐지 snort rule

alert tcp any any -> any any (msg:"Web_shell_Upload_php_passthru_func_Attack!"; content:"|0d 0a 0d 0a|<?php"; nocase; content:"passthru($"; nocase; sid:89868;)

![image](https://user-images.githubusercontent.com/52124043/61517162-8d327080-aa41-11e9-89ae-edf320af8cee.png)


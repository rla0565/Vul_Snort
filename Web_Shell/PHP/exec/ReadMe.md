Web_shell을 이용한 공격 탐지 snort rule(DVWA, weevely 이용)

weevely를 이용해 web_shell을 만들어 DVWA에 File upload

![image](https://user-images.githubusercontent.com/52124043/61447705-69612300-a98c-11e9-91e2-08f37de2a17b.png)

php web shell(exec함수) 탐지 snort rule

alert tcp any any -> any any (msg:"Web_shell_Upload_php_exec_func_Attack!"; content:"|0d 0a 0d 0a|<?php"; nocase; content:"exec($"; nocase; sid:89869;)

![image](https://user-images.githubusercontent.com/52124043/61516869-d7ffb880-aa40-11e9-9f94-9e5ca7b937b1.png)


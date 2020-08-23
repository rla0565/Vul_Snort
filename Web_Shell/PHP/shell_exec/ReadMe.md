Web_shell을 이용한 공격 탐지 snort rule(DVWA, weevely 이용)

weevely를 이용해 web_shell을 만들어 DVWA에 File upload

![image](https://user-images.githubusercontent.com/52124043/61448008-0ae87480-a98d-11e9-9e6a-877326441e50.png)

php web shell(shell_exec함수) 탐지 snort rule

alert tcp any any -> any any (msg:"Web_shell_Upload_php_shell_exec_func_Attack!"; content:"|0d 0a 0d 0a|<?php"; nocase; content:"shell_exec($"; nocase; sid:89866;)

![image](https://user-images.githubusercontent.com/52124043/61516992-244af880-aa41-11e9-9122-a54a66897e91.png)


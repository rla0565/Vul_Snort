XSS-document.write함수 이용 공격 방지 snort rule (DVWA이용)

![image](https://user-images.githubusercontent.com/52124043/61204558-741b7e00-a728-11e9-8b99-28e64a2bccdb.png)

url의 default 값의 인자로 script 삽입

snort rule : alert tcp any any -> any any (msg:"XSS-_ATTACK!"; content:"script"; nocase; content:"document.write("; nocase; sid:1234;)

![image](https://user-images.githubusercontent.com/52124043/61436061-eb455200-a974-11e9-8735-b470e900dbdb.png)

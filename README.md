# M5Stack_Core_RickRoll_WiFi
The raw packet demo of RickRoll - Compiles now for M5Stack - Core Grey.

Just compile and upload this sketch. Whenever the Core is turned on it produces several fake SSID's (WiFi access points) that produce the song lyrics:
```cpp
const char *rick_ssids[] = {        
  "01 Never gonna give you up",          
  "02 Never gonna let you down",       
  "03 Never gonna run around",        
  "04 and desert you",        
  "05 Never gonna make you cry",       
  "06 Never gonna say goodbye",       
  "07 Never gonna tell a lie",       
  "08 and hurt you"           
};        
``` 

![image](https://user-images.githubusercontent.com/1586332/128974953-7aab9497-ff96-4761-b16c-dd7489ba07ce.png)

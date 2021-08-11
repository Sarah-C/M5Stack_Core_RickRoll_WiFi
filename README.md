# M5Stack_Core_RickRoll_WiFi
The raw packet demo of RickRoll - Compiles now for M5Stack - Core Grey.

Right now the **esp_wifi_80211_tx** function has been patched (**in esp_idf file AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.6\tools\sdk\lib\libnet80211.a**) to prevent the transmission of several classes of packets (RickRoll SSID packets still work).           
That includes the "Deauth" packet that's been used for procuring WiFi passwords. The library now reports "Unsupported frame type: 0x0C."

Earlier versions of the library function were easily patched by removing the type checks, but more recent (July 2021+) builds have obscured the assembly making it much harder to patch. As a result - there's no current library patch that re-enables the freedom of esp_wifi_80211_tx().

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


Result:

![image](https://user-images.githubusercontent.com/1586332/128974953-7aab9497-ff96-4761-b16c-dd7489ba07ce.png)

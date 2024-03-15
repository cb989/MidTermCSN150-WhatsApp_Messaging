# MidTerm CSN150 - WhatsApp Messaging!
## Purpose:
Hello Prof! In my project, I setup the "CallMeBot API" in arduino using a random nerd tutorial with my ESP32 in order to send myself messages through WhatsApp using only the board. I found this sketch interesting simply because, well I can use my ESP32 to send me automated messages (with some tweaking to the code)! Its an amazing way to use your ESP32 to automate messages for something practical such as temperature sensing, the sky is the limit here really. The sketch works by sending an HTTP POST request to a custom API url that is provided by CallMeBot. By adding your own phone number, a message you want to send, and an API key also provided by CallMeBot when going through the motions of setting everything up, the CallMeBot API then simply sends you that message that you chose.
## Name of project:
ESP32 WhatsApp Messaging
### What equipment did I need??
* [The ESP32 Cam](https://www.amazon.com/Aideepen-ESP32-CAM-ESP32-CAM-MB-CH-340G-NodeMCU/dp/B0CMTVFCYD/ref=sr_1_13?sr=8-13)
* Random old USB type C cable I had lying around my house!
### Links to the documentation I used to do my midterm:
* [ESP32: Send Messages to WhatsApp](https://randomnerdtutorials.com/esp32-send-messages-whatsapp/)
* [Free API to Send Whatsapp Messages](https://www.callmebot.com/blog/free-api-whatsapp-messages/)
### Here are the exact steps I used in order to get the code working as per the random nerd tutorial:
1. First I had to add the CallMeBot phone number to my phone contacts.
2. I then had to message this number through whats app, saying "I allow callmebot to send me messages"
3. The bot sends you an API key when you send it the allow message, so I had to write that down.
4. Afterwards I had to open arduino, head over to sketch, include library, manage libraries, and then I had to search for and install "URLEncode library" by Masayuki Sugahara as shown in the turorial.
5. I then used random nerd's, (or Rui Santo's) sample code and put it into arduino.
6. In the code, there are several bits you have to change (such as the SSID) so here's exactly what I had to add:
   * My network SSID and Password
   * My phone number in interantional form
   * My API key that I recived after agreeing to be messaged by the CallMeBot API
   * And finally, I changed the message that I wanted to recieve to "Hello from ESP32 Cesar!".
7. Now I'm done. Pressed upload, and there you go. My own chosen message sent to me through the CallMeBot API using the ESP32 Board!
# Issues faced:
* Thanfully I only faced one small simple issue. I accidently typed my phone number in the format of "xxx-xxx-xxxx", when the API needed it in international format, meaning that I had to add the +1 before the number. I just went back through the random nerd tutorial and found what I did wrong, that was all! Overall smooth sailing.

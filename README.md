# App-Controlled-Guinea-Pig-Feeder
I created a guinea pig feeder that is controlled by an app on your phone or computer.

The guinea pig feeder app has three feed options: small portion, medium portion, and large portion

The app connects to my guinea pig feeder through a Wemos D1 Mini ESP8266 Wi-Fi Board and from there, a a 28BYJ-48
Stepper Motor with a ULN2003x Stepper Motor Driver spin the screw to dispense the food. 

The app was created through the MIT App Inventor. The app that I created has three different feed options. I will explain how one of them works.I first created an event handler that triggers once the button 
“feed” is clicked in the app. This feed corresponds to small portion size. “Feed2” is for the medium and “feed3” is the large portion size. Inside the "do" section is the code that executes when the Feed button
is clicked. First, it sets a variable called "Web1.Url" to a constructed URL. The URL is built by joining http:// protocol, the IP address of the feeder, and the /feed which is the endpoint of the server. It then
calls "Web1.Get" which sends an HTTP GET request to the URL that was just constructed. All this basically means that when the “feed” button is clicked in the app, it will send a web request to the Wemos D1 Mini 
ESP8266 Wi-Fi Board at the stored IP address with the "/feed" command. To connect the app to the board, you just type in the IP address of the board, and the app then connects to the board.

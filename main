if __name__ == '__main__':
    pass

#Define the imports
import twitch
import keypresser
import keyholder
t = twitch.Twitch();
k = keypresser.Keypresser();

#Enter your twitch username and oauth-key below, and the app connects to twitch with the details.
#Your oauth-key can be generated at http://twitchapps.com/tmi/
username = "username";
key = "oauth:";
t.twitch_connect(username, key);

#The main loop
while True:
    #Check for new messages
    new_messages = t.twitch_recieve_messages();

    if not new_messages:
        #No new messages...
        continue
    else:
        for message in new_messages:
            #Woohoo we got a message. Let's extract some details from it
            msg = message['message'].lower()
            username = message['username'].lower()
            print(username + ": " + msg);

            #This is where you change the keys that shall be pressed and listened to.
            #The code below will simulate the key q if "q" is typed into twitch by someone
            #.. the same thing with "w"
            #Change this to make Twitch fit to your game!
            
            #BeamNG.drive Nov. 17, 2021
            if msg == "throttle" or msg == "forward": keyholder.holdForSeconds("up_arrow", 4);
            if msg == "left": keyholder.holdForSeconds("left_arrow", 0.5);
            if msg == "reverse" or msg == "backward": keyholder.holdForSeconds("down_arrow", 2);
            if msg == "right": keyholder.holdForSeconds("right_arrow", 0.5);
            if msg == "stop1": keyholder.holdForSeconds("down_arrow", 1.3);
            if msg == "stop2": keyholder.holdForSeconds("up_arrow", 1.3);
            #if msg == "throttle" or msg == "forward": keyholder.press("up_arrow", 0.2);
            #if msg == "left": keyholder.press("left_arrow", 0.2);
            #if msg == "brake" or msg == "reverse": keyholder.press("down_arrow", 0.2);
            #if msg == "right": keyholder.press("right_arrow",0.2);
            if msg == "park": keyholder.press("p");
            if msg == "headlights": keyholder.press("n");
            if msg == "service": keyholder.press("m");
            if msg == "left signal": keyholder.press(",");
            if msg == "right signal": keyholder.press(".");
            if msg == "hazards": keyholder.press("/");
            if msg == "reset": keyholder.press("r");

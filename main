import json
import os
import sys
import time
import requests
import tls_client
import random
from colorama import Fore as fore

os.system("cls")



session = tls_client.Session(client_identifier="chrome112", random_tls_extension_order=True)

user = str(input("Channel Name > "))


info = f"https://kick.com/api/v1/channels/{user}"

banned_w = f"https://kick.com/api/v2/channels/{user}/chatroom/banned-words"



headers = {
    'accept': 'application/json',
    'accept-language': 'en_US',
    'connection': 'Keep-Alive',
    'content-type': 'application/json',
    'host': 'kick.com',
    'user-agent': 'okhttp/4.9.2',
    'x-kick-app-p-os': 'android',
    'x-kick-app-p-v': '28',
    'x-kick-app-v': '1.0.43'
}



sex = session.get(info, headers=headers)
niga = session.get(banned_w, headers=headers)


# USER INFO
slug = sex.json()["slug"]
follower_count = sex.json()["followersCount"]
ban_checked = sex.json()["is_banned"]
bio = sex.json()["user"]["bio"]
city = sex.json()["user"]["city"]
state = sex.json()["user"]["state"]
country = sex.json()["user"]["country"]
discord = sex.json()["user"]["discord"]
facebook = sex.json()["user"]["facebook"]
instagram = sex.json()["user"]["instagram"]
idd = sex.json()["chatroom"]["id"]
tiktok = sex.json()["user"]["tiktok"]
twitter = sex.json()["user"]["twitter"]
username = sex.json()["user"]["username"]
youtube = sex.json()["user"]["youtube"]

# CHATROOM INFO
channel_id = sex.json()["chatroom"]["channel_id"]
chatable_id = sex.json()["chatroom"]["chatable_id"]
chat_emotes_mode = sex.json()["chatroom"]["emotes_mode"]
chat_followers_mode = sex.json()["chatroom"]["followers_mode"]
follow_min_duration = sex.json()["chatroom"]["following_min_duration"]
message_interval = sex.json()["chatroom"]["message_interval"]
chat_slowmode = sex.json()["chatroom"]["slow_mode"]
chat_sub_mode = sex.json()["chatroom"]["subscribers_mode"]
channel_created_at = sex.json()["chatroom"]["created_at"]
banned_words = json.dumps(niga.json()["data"]["words"])




if chat_emotes_mode == False:
    chat_emotes_mode = "No"
else:
    chat_emotes_mode = "Yes"

if chat_followers_mode == False:
    chat_followers_mode = "No"
else:
    chat_followers_mode = "Yes"

if chat_slowmode == False:
    chat_slowmode = "No"
else:
    chat_slowmode = "Yes"

if chat_sub_mode == False:
    chat_sub_mode = "No"
else:
    chat_sub_mode = "Yes"


if bio == "":
    bio = None
else:
    bio = bio

if city == "":
    city = None
else:
    city = city

if state == "":
    state = None
else:
    state = state

if country == "":
    country = None
else:
    country = country


if discord == "":
    discord = None
else:
    discord = discord

if facebook == "":
    facebook = None
else:
    facebook = facebook

if instagram == "":
    instagram = None
else:
    instagram = instagram

if idd == "":
    idd = None
else:
    idd = idd

if tiktok == "":
    tiktok = None
else:
    tiktok = tiktok

if twitter == "":
    twitter = None
else:
    twitter = twitter

if youtube == "":
    youtube = None
else:
    youtube = youtube

if ban_checked == True:
    banned = "Yes"
else:
    banned = "No"
    

if sex.status_code == 200:

    os.system("cls")

    print(
f"""        
USER INFO:

Slug: {slug}
ID: {idd}
Created at: {channel_created_at}
Followers: {follower_count}
Banned: {banned}
Bio: {bio}
City: {city}
State: {state}
Country: {country}
YouTube: {youtube}
TikTok: {tiktok}
Twitter: {twitter}
FaceBook: {facebook}
Instagram: {instagram}
Discord: {discord}

CHATROOM INFO

Chatable ID: {chatable_id}
Emote Only: {chat_emotes_mode}
Only Follower: {chat_followers_mode}
Minimum Follow Duration: {follow_min_duration}
Message Interval: {message_interval}
Slow Mode: {chat_slowmode}
Subscribers Mode: {chat_sub_mode}
Banned Words: {banned_words}""")
time.sleep(120)

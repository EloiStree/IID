# IID Index Integer Date

Documentation of what is a IID  Index Integer Date. (A concept I created and is the base of my software(s) )


An IID is a value store on 16 bytes when received and 12 when sent.

It is design to allows remote control on shared server and to create IMMO.

(An IMMO is a integer massive multipy player)

**Index**
Index is the user on the server.
If negatif, the user is a guest
Else it is a registered user with a claimed index

Claim means that he is recogniazed by the server and validated as owner of the index in your shared server.

**Integer**
Integer is the value you want to share between your devices. 
It can be a simple action like:
- 42 = Turn on the light
- 0 = Shutdown all my computers
- -1 = Shutdown all my light
- ...

Or in a game:
- 123456789 Join the game share on the server
- 987654321 Confirm that you want to join the game shared on the server
- 0199887766 can be a use to remote control a drone 1 in the game 
- 1800000003 The user want to fire,  1800000099 user want to autodestroy

The idea here is to create library based on sharing integer of 4 bytes.
Note that the integer is under little endian format.

**Date**

By default the date is a ulong store in milliseconds UTC since 1970 sync on NTP.
If the first digit is 1 (1000000000000000000) the time is request to be executed at following time.

I wanted to use Ticks and make a difference between NTP and not NTP.
But it makes it complicated for no reason.
KISS 

**Conlusion**

All that to say.

I will take the time to write down some documentation in here.
But in all my software. That what is a IID.

Kind regards,
Eloi

License: [beerware license](https://en.wikipedia.org/wiki/Beerware)

Want to help me work on the the API around IID.

Feel free to send me donation, hire me as teacher or play my "Integer games" and "IMMO"





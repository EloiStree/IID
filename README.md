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

By default the date is a ulong store with the tick since 1970.

But,
- is it the date when to do the action or when it is sent ?
- is it the date of the computer or the one of a NTP ?

To specified we use a tag in front:
- 10 DateTime UTC when to execute on the remote
- 00 DateTime UTC when sent from the source
- 09 NTP Sent from the default NTP
- 08 NTP When to execute with default NTP

You can use the other digit to defined your own NTP custom time.

Losing the first digit means that you need to adjust the code every 316 Year.
Next adjustement is in 2286.8788501026693 starting from 1970 January 1er UTC.
As we have 99999999999999999 Ticks to use equal to 115740 days.


All that to say.

I will take the time to write down some documentation in here.
But in all my software. That what is a IID.

Kind regards,
Eloi

License: [beerware license](https://en.wikipedia.org/wiki/Beerware)

Want to help me work on the the API around IID.

Feel free to send me donation, hire me as teacher or play my "Integer games" and "IMMO"





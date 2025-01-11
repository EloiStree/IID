IID & 🍺.io: https://buymeacoffee.com/apintio - https://github.com/EloiStree/IID - https://github.com/EloiStree/apint.io

--------------------------------------

Rust version: [crates.io/crates/iid](https://crates.io/crates/iid)  
Python version: [pypi.org/project/iid42/](https://pypi.org/project/iid42/)  
C# version: [nuget.org/packages/be.elab.iid](https://www.nuget.org/packages/be.elab.iid)  
Unity OpenUPM: incoming
LUA: end-2025
Pico W version: soon

-----------

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

The date is a ulong in micro seconds

It max value is 18446744073709551615

The two first digit are the type and the rest is the date in mlliseconds
- 18 446744073709551615
  - 18 is the type
  - 253373149600000000 is year 9999
  - 400000000000000000 is the max value before having bugs
 
By default of this convention;
- 00 Means unkown date (developper did not or forget to specify)
  - If the next are 00, you can kind of guess:
    - 400000000000000000 
    - 000000001720342174 Seconds (
    - 000001720342174000 Milli seconds
    - 001720342174000000 Micro Seconds
  - 01: When sent in NTP date
  - 02: When to execute as NTP date
  - 03: When sent in local datetime utc
  - 04: When to execute in local datetime utc
  - 05-08: Undefined
  - 09: You don't need date you want bytes space extension
  - 
 If ou are able to use NTP in your code, try to use it.





**Conlusion**

All that to say.

I will take the time to write down some documentation in here.
But in all my software. That what is a IID.

Kind regards,
Eloi

License: [beerware license](https://en.wikipedia.org/wiki/Beerware)

Want to help me work on the the API around IID.

Feel free to send me donation, hire me as teacher or play my "Integer games" and "IMMO"




OpenUPM: 
Crates.io: https://crates.io/search?q=iid



Package in:
- My main language:
  - Python: https://github.com/EloiStree/IID_PythonPackage.git  https://pypi.org/search/?q=iid
  - Rust: https://github.com/EloiStree/IID_RustPackage.git  https://crates.io/search?q=iid
  - C# Console: https://github.com/EloiStree/IID_CSharpConsolePackage.git
  - Unity: https://github.com/EloiStree/IID_UnityPackage  https://openupm.com/packages/?sort=downloads&q=iid
  - Javascript
    - Local Webpage : Not done yet
    - Tamper Monkey :   Not done yet



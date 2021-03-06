
<h1 align="center">A Garden Irrigation System for Home Assistant (Version2)</h1>

__Please note that I recommend some understanding of Home Assistant in general and of Lovelace in particular if you choose to try this out.__

Apart from my instructions here, there are some 'real world' guides on how to set up and configure this package which were written by people who have done it. I will link to them here:

By @itajackass - [A guide for Italian people]( https://www.domoticadiy.it/2020/06/irrigazione-smart-my-garden-irrigation-home-assistant/) - perfectly readable using Google Translate and has been confirmed to work by another user.

By @bbogdanmircea - [Setup guide](https://github.com/bbogdanmircea/HA-Irrigation-Version2) - A fork of this project which uses more than the default maximum eight zones and also includes a general setup guide. It contains some good information but I understand that at the time of writing this it is not complete.


<h2>Prerequisites</h2>

There are some [prerequisites](https://github.com/kloggy/HA-Irrigation-Version2/blob/master/Pre-Requisites_Read_Me.md) to setting this up. PLEASE READ THEM. Any questions posted that look like they haven't been read may be ignored.


Please note that as it stands this assumes that you are using `yaml` mode for Lovelace because that is what I use.


<h2> Important Notes </h2>

Please understand that I am posting this project *purely as a way to share it* because people showed an interest in Version 1. It is *my personal solution* which I am more than happy for anyone to use in any way they see fit. I am prepared to help people get this working but only if you have shown that you have tried more than just copying the files. The prerequisites are documented and must be followed.

I am only using GitHub literally as a repository. What that means is I simply copy my code from my PC to here so that it can be shared. There is no formal version control here other than that inherent in the Github editing history.

One day maybe I'll delve further into how GitHub works but for now I'm afraid that is the situation.


<h2> More than eight zones? </h2>

I wrote this for use with up to eight zones but it can be quite easily adapted for use with more. I don't plan to change the code here to do this but @athan has done it and kindly allowed me to post a link to his branch.

If you need more than eight zones look [here](https://github.com/athan71/HA-Irrigation-Version2/tree/16-zones).

-----

<h2>Background</h2>

I wrote this package mainly because Version 1 of my irrigation package worked so well for me that the 'chief gardener' in this house (my wife!) decided she would really like to expand it from four zones to eight so as to include the flower beds as well as the lawn.

Whilst I believe that Version 1 could easily cope with this by the careful use of copy and paste I decided to do a complete rewrite.

One reason for this decision was that Version 1 had been one of the first things I did with HA and I always thought that there were things I could have done better. Furthermore, Lovelace appeared since then so there is scope to do much more with the user interface.

Also, being early 2020 many of us found ourselves with too much time on our hands due to the Corona virus so it seemed like a perfect project to pass some of the time.

As I was writing it I was also learning new techniques in Lovelace from the forum so this became as much a project about the user interface as it did about the irrigation.

But... I am by no means a Javascript or CSS programmer so there may well be things I (or you) can improve on at some point in the future. 

Version 1 was designed around a Sonoff 4ch but for Version 2 I will use an 8 relay board controlled with an ESP32.
This in itself should make little difference as ultimately all the package does is turn switches on and off.

This package has been designed with two scheduled cycles per day with each cycle having up to eight zones and all zones can be scheduled to run on any day(s) of the week.

A manual cycle is also provided.

The watering times can be automatically adjusted based on rainfall and temperature and whilst I think this has been improved in Version 2, as in Version 1 this is quite experimental. It is different to (better than) Version 1 in that both the rainfall and temperature adjustments can be turned on or off independently of each other and separately for each cycle and the sensors can easily be configured to use any weather source you choose.

Almost everything can be set from the UI including the friendly names of cycles and zones. Tap/click on fields to change them in a pop-up (but remember that if you have several browser tabs open the pop-ups may appear on a different tab!). 

__Note -__ Extensive use is made of `!include` to avoid code repetition. You need to replicate the folder structure in order for it to work. You can change the lovelace code if it suits you to have your own folder structure but I can't help if you choose to do that.

As it stands you need a `lovelace` folder and of course the usual folder that your packages are in.

(See the following documentation for [packages](https://www.home-assistant.io/docs/configuration/packages/) and [Lovelace](https://www.home-assistant.io/lovelace/dashboards-and-views/)).

--------------

__Disclaimer__ - I have been using this package now for a few weeks and whilst I do not use all the features I am confident that it all works as it has now also been used by some other people. Feel free of course to use, adapt or change it in any way you see fit. But if you do find errors I'd be interested to know so I can look at it although no promises can be made regarding how or when I will get to fix anything.


Likewise if you come up with any improvements also please tell me!


<img src="https://github.com/kloggy/HA-Irrigation-Version2/blob/master/screenshots/screenshot-v2.png">

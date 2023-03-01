# Voidworks Inc. Hacking Tutorial - Phishing
## Difficulty: So easy that it's scary. [=⭕==================] (10%)
<br>

![LetDowntoVoid-Logo-Dark](https://raw.githubusercontent.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/main/Phishing/Images/LetDowntoVoidFull.png#gh-dark-mode-only)

![LetDowntoVoid-Logo-Light](https://raw.githubusercontent.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/main/Phishing/Images/LetDowntoVoidFull_black_end.png#gh-light-mode-only)

<br>

### <br>**Note**: ***This is just a tutorial so that people understand how this system works. Please do note hack anyone without there consent and this is just a tutorial for education purposes and a way to learn how to stay safe.***

#### <br> Made with 💖 by LetDowntoVoid with the belief that everyone should know Information Technology.

____________________________________________________________ 

## <br>Terms of Service (ToS)

+ The author provided these AS IS and is not to be changed in any form or way. 

+ The author made with the belief that people must be able to understand the internet and the ways to stay safe. They believe that people have the right to stay safe and also have the right to know what happens. 

+ The author will ***NOT*** be responsible for any attacks caused because as he mentions: **These tutorials are meant for education purposes only. _DO NOT HACK ANYONE WITHOUT THEIR CONSENT AND PLEASE NEVER HACK (ETHICALLY AT THAT) IN OPEN INTERNETS._**

+ The author will not be responsible for any damage caused either. 

+ User has to hack ethically. Any penalties caused for hacking unethically or hacking with an intention of causing harm will not be the responsibilty of the author. 

## <br>Safety to be taken while hacking:

+ Use a virtual machine. Run a Virtual Machine on a free software. The author recommends a software like VMWare or VirtualBox. Preferred is VMWare as it is easier to use.

+ Always ALWAYS use a VPN. A free one is fine but always go for a VPN whatever you do. A Proxy for doing the hacking is also fine. But that being, advanced, might make beginners confused. 

+ Always have a proper target.
    - Make sure your target knows that you will be hacking them. The Target must be not only informed but the target must also give their consent for you to hack them. 

## <br>Requirements:

+ A Virtual Machine Software like [VMWare](https://www.vmware.com/in.html "The Author uses this one. Easier to understand and work with.") or [Virtual Box](https://www.virtualbox.org)

+ Linux Virtual Machine (Any Distro is fine. The author will be using [Kali](https://www.kali.org/get-kali/ "Kali is a powerful linux distro meant for Penetration. Debian based.").)

+ Some skills with UNIX is preferred.

+ A ready Virtual Machine environment. There are good tutorials on youtube that you can use to set up a Virtual Machine env. 

+ Get used to with virtual machines.

### <br>The author also recommends you learn about the following things:
+ UNIX Scripting
+ Tunnelling
+ Setting up a Virtual Machine 


## <br>Time for the real stuff: 

### Step 1: Start up your Virtual Machine Software and your Virtual Machine with a Linux Distro
<br>
<img src="https://github.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/blob/main/Phishing/Images/ImageVMWare.png?raw=true">
<center> VMWare: The software the author is using to host a virtual linux machine </center>

<br>

Wait for your machine to load in.

<br>

<img src="https://github.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/blob/main/Phishing/Images/KaliMainScreen.png?raw=true">

<center> Kali mainscreen </center>

<br>

### Step 2: Sign up for an Ngrok Account
<br> 

Sign - up for a free account at [Ngrok - A tunneling System](https://https://ngrok.com). This will allow the tool we will later use (blackeye-im) to creat a fake tunneling website that will send us the details the victim has entered along with their IP address!


<br>
<img src="https://github.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/blob/main/Phishing/Images/downloadNgrok.png?raw=true">
<center> The Ngrok dashboard after signing up </center>
<br>

### Step 3: Going to the github page of the tool we will be using -  `blackeye-im`
<br>

Go to the GitHub Page of [Blackeye-im](https://github.com/thewickedkarma/blackeye-im). It is a powerful tool used for phishing. Copy the link as it will be used to clone (that is to say install) on our computer.

<br>
<img src = "https://github.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/blob/main/Phishing/Images/githubBlackeye_im.png?raw=true">
<center> The Blackeye-im Github Repository. Credits to @thewickedkarma </center>
<br>

### Step 4: Install `git` using `sudo` to clone the repo.
<br>

It's now time to look like a professional hacker! Open `terminal` (command prompt / powershell equivalent of Linux).

As you open the terminal, first command we execute is 
    
    sudo apt install git
It will ask your for your `sudo` password which is the password you set up for sudo.

<br>
Then you type this  
<br>
    
    git clone https://github.com/thewickedkarma/blackeye-im

<br>

This will install (clone) the repository on your computer in a folder named ` blackeye-im `.
<br>

### Step 5: Setting up Ngrok for `blackeye-im`

<br>

Go to your [Ngrok Dashboard](https://ngrok.com) and search for something named `Connect your account`

<br>

<img  src="https://github.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/blob/main/Phishing/Images/AuthTokenCopy.png?raw=true">
<center> 'Connect Your Account' in Ngrok Dashboard </center>

<br>

Copy that. Now we will go to the path / directory where the `blackeye-im` repository is stored. And of course we will be using the terminal!

<br>

We will go to the terminal and type in this 

    
    ls

The command `ls` gives us the list of the files and the folders in this location.

It should list out `blackeye-im` as one of them

Then we will execute this command

    cd blackeye-im

This will move the terminal's acting location into the directory where `blackeye-im` repository is stored.

<br>

<img src="https://github.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/blob/main/Phishing/Images/blackeye_dis.png?raw=true">
<center>The above 2 commands in action</center>

<br>

Now here we will execute an intersting command

When we copied the command from the Ngrok Dashboard, we copied something like this

    ngrok config add-authtoken <random-string-of-letters-and-numbers>

This random string of letters and numbers is actually your `authtoken`. A token that is used by Ngrok to know that your account will be used!

<br>

Now in the terminal we will execute this command
    
    ./ngrok authtoken <authtoken>

Here you will insert the `authtoken` that was given to you by ngrok in the place of `<authtoken>`.

<br>

<img src="https://github.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/blob/main/Phishing/Images/AuthtokenCMD.png?raw=true">
<center> The command that should be in the end </center>

<br>

### Step 6: Actually starting the hack now!

Now we have reached the last step of actual work from our side: starting the "shell script" of `blackeye-im`!

In the terminal just type this

    ./blackeye.sh

And **BAM**! The program started. It present you a menu. A list of websites that you will choose 1 from. What it will do is that it will clone that website to make it look real so that the victim does not get suspicious of the fake site. 

You type the number for example I type `1` to clone Instagram's Login Page. 

Then it will ask which tunneling system we will use. It gives us 2 options 
+ Ngrok
+ Local Tunnel

We obviously type `1` because we will be using Ngrok!

It will do the rest on its own and it will present you will a weird looking link. This is the link you will send to the victim!

As the victim opens the link, their IP is sent to you. If the victim falls for the website and tries to log in, the details will be immediately sent to you in the terminal! 

The link looks very funny and sussy so we can use url shorteners like `TinyURL` to make it not so sus... 

<br>

<img src="https://github.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/blob/main/Phishing/Images/FinalOutput.png?raw=true">
<center> The menu presented and options the author chose. </center>

<br>

### Step IDKWHATITWAS: Wait 

Hacking is a game of waiting and patience. You have to wait for the victim to open! And As they do the result will be immediate!

<br><br>

## And that's it! You now know how to do a phishing attack on someone!

Make sure you hack ethically and do read the ToS. This is a very sesitive world and you get fined if not done safely or done in a manner to harm people! Again, ***THE AUTHOR WRITES THIS ON THE BELIF THAT PEOPLE MUST KNOW ABOUT THE INTERNET AND HOW THINGS ARE DONE AND HOW THEY CAN BE SAFE ON THE INTERNET!***

<br>

### Next tutorial will be on *Phishing Emails and People engineering!*

#### Thanking you with best regards,

![LetDowntoVoid-Logo-Dark](https://raw.githubusercontent.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/main/Phishing/Images/LetDowntoVoidFull.png#gh-dark-mode-only)

![LetDowntoVoid-Logo-Light](https://raw.githubusercontent.com/LetDowntoVoid/VoidWorksInc-hackingTutorials/main/Phishing/Images/LetDowntoVoidFull_black_end.png#gh-light-mode-only)

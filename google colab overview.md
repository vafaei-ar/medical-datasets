# Google Colab Overview
## Disclaimer:
The aim of this document is not to be a tutorial on Google Colab; there are many tutorials out there covering many aspects and reinvention of the wheel is just an exercise in futility. Instead, it is going to provide an overview of *some* Google Colab's capabilities which might be helpful.

It is similar to the jupyter notebook, however, shortcuts are different and the menus are designed to access Google Colab's options such as activating GPU or TPU. A piece of prior knowledge of jupyter notebook might be helpful but you have to spare a few minutes to explore the menus (do not forget about side-bar menus) and shortcuts; it is colab notebook not jupyer notebook after all!

* Colab notebooks are running on the top of a Linux virtual machine instance.
 * The instance will be terminated after 12 hours, or after 90 minutes if the session disconnected (e.g. you close the window or because of the session idle timeout). 
 * You can run linux command starting with `!`: 

![uname](/pics/linux.png "Linux")

![distro and version](/pics/ubuntu.png "Ubuntu")


  * You have root access:

![root](/pics/root.png "Root")

  * And internet access:

![internet](/pics/internet.png "Speed test")

* A fair amount of workstation-class CPU, ram, and GPU for free:

![cpu](/pics/cpu.png "cpu")

![ram](/pics/ram.png "ram")

![gpu](/pics/gpu.png "gpu")

* GPU is not enabled by default, [Here how you can enable GPU or TPU](https://lmgtfy.com/?q=how+to+enable+GPU+or+TPU+on+google+colab)

 
* [You can assess your google drive files with relative ease!](https://lmgtfy.com/?q=how+to+access+google+drive+in+google+colab)
 
 * [Or upload from your computer](https://lmgtfy.com/?q=upload+file+from+computer+to+google+colab&s=t)
 
 *  Additionally, you could access other cloud storage (like Mega Upload) but the transfer speed could vary! (I am sure you don't need to someone google it for you ;))
 
*  Furthermore, it is possible to download data from Kaggle directly. To make it possible, you have to verify your kaggle account with a phone number.
 
* Remember! you have access to a Linux command line + root access + internet! so the sky is your limit.
 
* There is a way to access that Linux instance directly through your own Linux terminal. To link your system terminal to Google Colab’s Linux First copy/paste the code in  [this code](https://gist.github.com/IAmSuyogJadhav/0371b90411746f91513c6ccc25274aa0) into Google Colab and run. Authorization token is required; follow the instructions, the result would be like:

![ngrok](/pics/ngrok.png "ngrok")

Open your terminal and modify your public address, in our case, like this: `ssh root@0.tcp.ngrok.io -p 14765`(beware of a few changes) and enter the password.

Two points:

1)  If you have a slow connection the connection may not be established.
2) If the connection remains IDLE for about 30 mins (e.g. you don't issue any command which might happen when the process takes long ) it would be disconnected so it is better to run commands with verbose option (usually with -v flag).


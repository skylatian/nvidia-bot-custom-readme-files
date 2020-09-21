**__Nvidia Sniper Install:__**

1) install firefox normally
2) download geckodriver https://github.com/mozilla/geckodriver/releases
3) install git: https://git-scm.com/download/win
4) Download Python 3.8.x **__64bit__** https://www.python.org/ftp/python/3.8.5/python-3.8.5.exe
save gecko and sniper in the same folder for convenience 

__**Install python:**__
Run installer and customize the install
-Hit next
:ballot_box_with_check: check `add python to environment variables`
-go ahead with the rest of the install

__**Geckodriver install/addition to PATH**__
-unzip geckodriver, copy the directory (This should be the folder with the .exe in it, ex: `C:\Users\user\desktop\gecko\`, with the geckodriver.exe being located in folder `gecko`)
-search in windows search `edit system environment variables`, open it
-click environment variables
-under system variables, edit the `Path` variable
-click new, paste the geckodriver directory you copied earlier
-ok
-ok
-ok

__**Pipenv install**__
-Go to the directory you want to have sniper located, and type ` cd [path to location]` in command prompt.
-type `git clone https://github.com/philippnormann/nvidia-sniper.git`
- this will create a solder called `nvidia-sniper`
-open a command window, type:
-` cd [path to nvidia-sniper folder]` ex: `cd c:/desktop/nvidia-sniper`
-type `pip install pipenv`
-wait for this to finish
-type `pipenv install`
-wait again
-type `pipenv install windows-curses`
-Done :white_check_mark: 

__**Sniper Setup:**__
-open to `customer.json` in the `nvidia-sniper/data` folder
-**To stop firefox opening in Dutch,** Change "locale" to your own (`en-us` for USA) This is just for country, not state. Note: this is different from your country code. **ONLY CHANGE TEXT WITHIN QUOTES" "**
-save

__**Running Sniper**__ 

open a command window within the `nvidia-sniper` folder (just like before with `cd c:/....`)
- type: `pipenv run python -m sniper`
-Select the card to monitor, and it'll periodically refresh a webpage in Firefox checking for stock.

__**TEST TEST TEST**__ 

Open customer.json again: 

**ONLY CHANGE TEXT WITHIN QUOTES" "**

-Put in your address. **Note:** State is not required for some reason.
-Select an rtx-2060-super to make sure everything is working. Nvidia will likely suggest a modified address, use that to streamline the process (for example, they prefer `Drive` to be `Dr`). Continue to modify your address until the suggestion disappears when the bot is run again. If it’s not there in the first place, congratulations, you’ve pleased the gods. Have a cake :birthday: 

-Once the process gets to a screen that looks like the screenshot below without interruption, you're all set! Put your payment info in `customer.json` now and get ready for launch!

__**Updating**__

**__MOVE any modifed files out of `nvidia-sniper`__** (customer.json mainly) THEY WILL GET REMOVED in the update process

-open cmd
-tpye ` cd [path to nvidia-sniper]` ex: `cd c:/desktop/nvidia-sniper `
-type `git pull`
-exit the window

## Automated backup of USB contents to cloud
I work on a few different computers for my lesson plans, PPTs, handouts, etc. - and I want to be sure that I have a backup of this stuff (as you'll see in another tip, I almost lost several PPTs when my USB got bent).

Need EasyRoboCopy from http://www.tribblesoft.com/home-page/easy-robocopy/easyrobocopy-v1-0-14/; EasyRoboCopy provides an interface for RoboCopy (command line, built into Windows).

<img src="img/Annotated.png" class="inline"/>
1. Your USB source
2. Your destination source (make sure your cloud sync program knows to upload this folder).
3. Copy all subdirectories (not just everything in the "home" folder of the USB), even if they're empty.
4. Try again if there's a problem.
5. If a file on the USB is older than the "same" file in the cloud-sync folder, don't replace the cloud-sync version.
6. Make things run a bit faster.
7. You could set the maximum bytes to 10000000 (10,000,000 = 10MB) - but you'll big videos, some songs, some PPPTs etc. this way.
8. Make the program check for updates every (1) minute, and copy if there's an update.
9. Start copying.

TODO: 
- Start copying/monitoring when USB is inserted. [https://superuser.com/a/845411/485752 - starts at boot]
Note5: 
1. rename USB (e.g. JCUSB)
IMAGE^
2. in Powershell script have `if ($driveLabel -eq 'JCUSB')`
2. in Powershell script have `start-process "C:\Users\middo\OneDrive\USBsync.bat"`
3. Save powershell as .ps1 file in cloud-sync folder (C:\Users\middo\OneDrive\ELA) 
4. Create .bat file in cloud-sync folder (C:\Users\middo\OneDrive\ELA) (TO DO)
5. Copy-paste the Command-line code from EasyRoboCopy into the .bat file (for me, this is `ROBOCOPY.EXE "U:\ELA Lessons" "C:\Users\middo\OneDrive\ELA\ELA Lessons" /E /DCOPY:DAT /PF /XO /R:2 /W:3 /MT`)
- Note: `start /min ROBOCOPY.EXE "U:\ELA Lessons" "C:\Users\middo\OneDrive\ELA\ELA Lessons" /E /DCOPY:DAT /PF /XO /R:2 /W:3 /MT` will minimise the RoboCopy window - very nice!
6. In Task Scheduler, create a task:
- [Trigger] = Log on of user 
- [Action] = Start a program, 
- Program/script = `powershell`
- Add arguments (optional) `C:\Users\middo\OneDrive\ELA\USBSync.ps1`

**NOTES** 
- Change USB letter to U
^ IMAGE


- Stop the copying/monitoring when the USB is removed.




## The dangers of sliding whiteboards
One of my schools has a smart TV (great!) with front-facing USB ports. I have my USB stick attached to my keys, and the extra little distance meant that caused a board to snag when I slide it towards the screen. My USB stick got bent and didn't work - so I hit it with a screwdriver base until it'd fit in a USB slot; fortunately, it still worked (despite every computer claiming there's an error when I plug it in!).

Tips: 
*keep USB sticks separate from keychains (though that makes them easy to lose), 
*remove them from the smart screen once your PPT has loaded. To make up for potentially having to reinsert your USB in a class, you can make shortcuts to your relevant lessons in the main directory of the USB - so you have fast access to your PPTs (whilst maintaining your file structure of choice).
*some smart TVs may have USB extension/adapter devices at the side/back. Use them if you can!

### Todo: Don't forget to register to vote 
https://www.gov.uk/register-to-vote 

"British citizens living abroad
You can register as an overseas voter for up to 15 years after leaving the UK, as long as:

-you’re a British citizen
-you were registered to vote in the UK within the previous 15 years (or, in some cases, if you were too young to have registered when you left the UK)
Just register to vote in the normal way. You’ll need to renew your registration every year."
 from https://www.gov.uk/voting-when-abroad

### Todo: Student Finance England (SFE) - student loan repayments 
http://www.studentloanrepayment.co.uk/portal/page?_pageid=93,6678653&_dad=portal&_schema=PORTAL
n.b. if this link doesn't work, search for "student finance england abroad"


### Todo: Essential Chinese for the classroom (for lower grades)

### Todo: Checking mobile data usage on China Unicom

### Todo: WeChat location sharing to meet up with your friends




Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/IdiosApps/ShanghaiTeacherTips/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

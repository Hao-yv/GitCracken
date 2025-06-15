To apply the patch, yarn must be installed on the system.
On Windows, you need to install https://nodejs.org/dist/v16.14.0/node-v16.14.0-x64.msi or https://nodejs.org/dist/v16.14.0/node-v16.14.0-x86.msi and run npm install --global yarn
On Linux, it is installed from the repositories.

Install GitKraken, go to the GitCracken folder and run the commands:
The code:
	yarn install
	yarn build
	node ./dist/bin/gitcracken-patcher.js (Inside Crack -> GitCracken folder)

In hosts add: 0.0.0.0 release.gitkraken.com

If after restarting GitKraken PRO the version is still missing, you need to delete the local profile: %appdata%\.gitkraken for Windows, ~/.gitkraken for Linux or macOS

On MacOS, you must run GitKraken before patching, otherwise MacOS will mark the application as broken.
If the application was patched without running it first, run sudo xattr -rd com.apple.quarantine /Application/GitKraken.app

 Installation on Windows 7
I fought for a very long time, I was able to grunt under Windows, moreover, under 7-ku. I'm writing here so I don't get lost.
1. Download nodejs from here: https://nodejs.org/en/download/releases/ , while under 7-ku there must be version 13.0.0 or lower, in higher versions support for 7ki is discontinued, she swears. Why exactly this version, you can read here: https://stackoverflow.com/questions/62212754/nodejs-for-windows-7 . It also says how you can bypass the Windows version check in order to install the latest version of nodejs.
2. Install nodejs. Installation is described here: https://www.liquidweb.com/kb/how-to-install-yarn-on-windows/. I agreed to install all related components just in case, so that there were no dependency errors.
3. Pull jarn. Moreover, the surprise is that not every release contains the *.msi file for Windows. I do not remember how, but I found that the installer is contained, for example, in this version: https://nightly.yarnpkg.com/yarn-1.23.0-20200615.1913-unsigned.msi
4. Install. Installation is described here: https://www.liquidweb.com/kb/how-to-install-yarn-on-windows/. I agreed to install all related components just in case, so that there were no dependency errors.
5. Quack according to the attached instructions. Those. run 3 magic commands from the GitCracken folder:
yarn install
yarn build
yarn gitcracken patcher OR node ./dist/bin/gitcracken-patcher.js

It must be borne in mind that the Internet is required for paragraph 5.

I had a goal to generally make the krakin work on a wheelbarrow without an Internet. At first I had to quack everything on a wheelbarrow with an Internet, and then do the substitution of folders on a wheelbarrow without an Internet. To do this, after hacking and registering in your account, you will need to transfer the folders
C:\Users\<your profile folder>\AppData\Local\gitkraken
C:\Users\<your profile folder>\AppData\Roaming\.gitkraken
C:\Users\ <your profile folder>\AppData\Roaming\GitKraken
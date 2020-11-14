# Food App UI Part  - Figma to React Native
## Bug fixing: React native ERROR Packager can't listen on port 8081
```
On a mac, run the following command to find id of the process which is using port 8081
sudo lsof -i :8081
Then run the following to terminate process:
kill -9 23583
```
[React native ERROR Packager can't listen on port 8081](https://stackoverflow.com/questions/43425754/react-native-error-packager-cant-listen-on-port-8081)   

## Adding custom fonts 
[Ultimate guide to use custom fonts in react native](https://medium.com/@mehrankhandev/ultimate-guide-to-use-custom-fonts-in-react-native-77fcdf859cf4)   
 
## npm install really low
1.Switch your node version to the  node v11.10.0 (npm v6.7.0):
```
source ~/.bash_profile 
nvm ls-remote 
nvm install   v11.10.0 
cd /Users/zt/foodappui 
npm install
```
[使用nvm管理node与npm版本](https://juejin.im/post/6844903861157642247)  

2.Then change your internet to the Mobile data  

3.If it necessary, change the bash profile like remove the path below, then run the process above: 
```
open ~/.bash_profile
export ANDROID_SDK=/Users/zt/Library/Android/sdk

export PATH=/Users/zt/Library/Android/sdk/platform-tools:$PATH
```
[Why is “npm install” really slow?](https://stackoverflow.com/questions/41524903/why-is-npm-install-really-slow)  
[How do I edit $PATH (.bash_profile) on OSX?](https://stackoverflow.com/questions/30461201/how-do-i-edit-path-bash-profile-on-osx)  

## Run the code in the simulator, when you shut down the editor.
```
source ~/.bash_profile  
nvm use v11.10.0 
nvm use v11.10.0 
```
## image resource download
You could either download it from the github by using the Gitzip or utilize the Figma to get the image resources


## Reference:  
[Food App Design - Figma Tutorial](https://www.youtube.com/watch?v=jA-R8bJRZPg&ab_channel=MadeWithMatt)  
[Food App UI Part 1 - Figma to React Native](https://www.youtube.com/watch?v=7_nsd_iNDtY&ab_channel=MadeWithMatt)  
[Food App UI Part 2 - Figma to React Native](https://www.youtube.com/watch?v=GPu1ax1Fga0&ab_channel=MadeWithMatt)  
Source code [FoodAppUI](https://github.com/mattfrances/FoodAppUI)  
export ANDROID_SDK=/Users/zt/Library/Android/sdk

export PATH=/Users/zt/Library/Android/sdk/platform-tools:$PATH
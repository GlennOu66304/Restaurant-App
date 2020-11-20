# Food App UI Part  - Figma to React Native
## How to put the local prohject into git hub:
1. As for the code, you need to drag the file into the empty project which you build from Github; 
2. Drag the Readme file too.  

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
npm run ios 
```
## image resource download
You could either download it from the github by using the Gitzip or utilize the Figma to get the image resources

## shift in the two screen page of app, you need to utilize the React Native Navigation:
[React Navigation](https://reactnavigation.org/docs/getting-started)   

## React Native syntext quick references:  

1.You need to type the key word + React Native doc into the Google search bar to pick the content to quick refernece, and put the unknow part into the github, and the link as maiin references.

Such as"View" View React Native doc
Main references:  
[View](https://reactnative.dev/docs/view)  

2. To type the code into the editor, you need to wait for the one function finish, then start to add the code into your editor and try to understand the code.  

## Style React Native understand:
1. In order to use the style to customized your design, you need use style(CSS) to acieventit. first to import it from the react native, then add the style content into the view or text to define a name.  
```
import { StyleSheet, Text, View } from 'react-native';
<View style={styles.container}>
        <Text style={styles.red}>just red</Text>
```

2. in the code specific details, first you need to define and name in the view or text, then go to a certain section to add the style content to add the style value to change it.
```
const styles = StyleSheet.create({
  container: {
    marginTop: 50,
  },
```

[Style](https://reactnative.dev/docs/style)   

## Reference:  
[Food App Design - Figma Tutorial](https://www.youtube.com/watch?v=jA-R8bJRZPg&ab_channel=MadeWithMatt)  
[Food App UI Part 1 - Figma to React Native](https://www.youtube.com/watch?v=7_nsd_iNDtY&ab_channel=MadeWithMatt)  
[Food App UI Part 2 - Figma to React Native](https://www.youtube.com/watch?v=GPu1ax1Fga0&ab_channel=MadeWithMatt)  
[Food App UI Part 3 - Figma to React Native](https://www.youtube.com/watch?v=Z7UjnkbbIqk)  
Source code [FoodAppUI](https://github.com/mattfrances/FoodAppUI)  
Link to Figma file[Figma file ](https://www.figma.com/file/gfIboy4J44lvD9CoDr62rH/Food-App?node-id=0%3A1)   
export ANDROID_SDK=/Users/zt/Library/Android/sdk

export PATH=/Users/zt/Library/Android/sdk/platform-tools:$PATH
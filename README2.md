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


## View Syntext  
1.View is baciclly like the div in the html, some sort of the Html lay out potion text:

2. You need to import the view first, then 
```
import { View, Text } from "react-native";
```

3. You have two ways to utilize the Viwe
First you could utlize the <View> & </View> to bracket the code block;   
```
<View
        style={{
          flexDirection: "row",
          height: 100,
          padding: 20
        }}
      >
 </View>
```
Second you could simply add slash "/" at the end of the <View>;  
```
<View style={{ backgroundColor: "blue", flex: 0.3 }} />
```
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
[Styling in React Native: Step By Step](https://medium.com/better-programming/styling-in-react-native-step-by-step-540f57411566)
## Second weay to customize your lay out, similiar function like"Sytle"
You don't need import sylesheet from the react native, just add the value into the View and the text:  
```
<View style={{flex: 1, flexDirection: 'row'}}>
```
[Layout with Flexbox](https://reactnative.dev/docs/flexbox) 

3.As for the bugs in the React Native console, you need to make sure that you type the cortrect CSS name to change it.  

# Change the wrpper's color

You need add new style rules into the wrapper, the rules should be like a boolean secelction.  
1.To add more style rules, you simply create an array  
```
<View style={[
            styles.categoryItemWrapper,
            ]} >
            </view>
```
2. Change the wrpper's color
```
styles.categoryItemWrapper,
            {
                backgroundColor:item.selected? colors.primary : colors.white,
            }
            ]} >
```

## Bugs, Could not see the search text in the search bar

You need delte the flex:1 in the style section, or try the solution to solve this issue.   
[React native text going off my screen, refusing to wrap. What to do?](https://stackoverflow.com/questions/36284453/react-native-text-going-off-my-screen-refusing-to-wrap-what-to-do)  
[[Text] Text doesn't wrap #1438](https://github.com/facebook/react-native/issues/1438)  
[Flex box in react Native is not working buttons wont show up](https://stackoverflow.com/questions/58868460/flex-box-in-react-native-is-not-working-buttons-wont-show-up)  
[Layout with Flexbox](https://reactnative.dev/docs/flexbox)   

## Bugs: Could not see Font Family changes in the app:

Do not add the extra s into the style in the View while you define the Viwe:
```
 <Text style={styles.categoriesTitle}>Categories</Text>
```
## ReactNative FlatList understand:  
Falst is kind of tool that allow you reden the data into a list in the app layout.  
1.To use this tool, you need to load the data from the external file or just put the data into the current file:  
```
const DATA = [
  {
    id: 'bd7acbea-c1b1-46c2-aed5-3ad53abb28ba',
    title: 'First Item',
  },
]
```
2. Then according to the syntext rules to add the required content:  
```
<FlatList
        data={DATA}
        renderItem={renderItem}
        keyExtractor={item => item.id}
      />
```

To allow render the data's layout, you could set the prop horizontal of the FlatList to achive this
```
horizontal={true}
```
Main references:  
[FlatList](https://reactnative.dev/docs/flatlist)  

## Const in the React Native:  
It just build another function allow you to intreract with the code. 

1.To use this function,you need to import the react first and related other Core component
```
import React from 'react';
import { Text } from 'react-native';
```
2. Then build a componet as below:  
```
const Cat = () => {
  return <Text>Hello, I am your cat!</Text>;
};

export default Cat;
```
## Bugs Error: Text strings must be rendered within a <Text> component.

You need to put the following code into the <FlatList /> inside.
```
 data={DATA}
        renderItem={renderItem}
        keyExtractor={item => item.id}
```
Main references:  
[Your first component](https://reactnative.dev/docs/intro-react)  
## ReactNative image understand 

Image in the React Native allow you put the image into it.  
To utilize the image, you need to import it from the reactNative first, then
```
import { View, Image, StyleSheet } from 'react-native';
```
You need to add the source to load the external image source:  
```
<Image
        style={styles.tinyLogo}
        source={require('@expo/snack-static/react-native-logo.png')}
      />
```
Main References:  
[Image](https://reactnative.dev/docs/image)  

## Load the data from external file:  
Item + dot + specfific content in the bracket from the external file to load it:  
```
{item.image}
{item.title}
```
[Fetching Data in React Native](https://medium.com/@alialhaddad/fetching-data-in-react-native-d92fb6876973)  

## Bug: if you could not see the item wrapper change, you need to go to the color.js file to add the whiter and black color value:
```
white: '#FFF',
black: '#000',
```
## they way to allow the list move in the wrapper:  
```
marginLeft: item.id == 1 ? 20:0,
```
## Utilize the Map to render the popularData
,map() is like for loop function in the Pure Javascrip, it will allow you loop the data do repeattation work.  

To use .map() you need to have the data
```
const numbers = [1, 2, 3, 4, 5];
```
then you need to defie a new const 
```
const doubled = 
```
Connect the orginal 
```
const doubled = numbers.map((number) 
```
assign the function which you want to interact with the data  
```
const doubled = numbers.map((number) => number * 2);
```

[Lists and Keys](https://reactjs.org/docs/lists-and-keys.html)   
## Reference:  
[Food App Design - Figma Tutorial](https://www.youtube.com/watch?v=jA-R8bJRZPg&ab_channel=MadeWithMatt)  
[Food App UI Part 1 - Figma to React Native](https://www.youtube.com/watch?v=7_nsd_iNDtY&ab_channel=MadeWithMatt)  
[Food App UI Part 2 - Figma to React Native](https://www.youtube.com/watch?v=GPu1ax1Fga0&ab_channel=MadeWithMatt)  
[Food App UI Part 3 - Figma to React Native](https://www.youtube.com/watch?v=Z7UjnkbbIqk)  
Source code [FoodAppUI](https://github.com/mattfrances/FoodAppUI)  
Link to Figma file[Figma file ](https://www.figma.com/file/gfIboy4J44lvD9CoDr62rH/Food-App?node-id=0%3A1)   
export ANDROID_SDK=/Users/zt/Library/Android/sdk

export PATH=/Users/zt/Library/Android/sdk/platform-tools:$PATH
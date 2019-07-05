---
title:  "React Localisation!"
subtitle: "Use React localisation corresponding to various business types"
author: "Snehal Patil"
avatar: "img/authors/snehal.png"
image: "img/react.png"
date:   2019-07-02
---


A simple localisation for react app can be provided using the flow as shown in image below 

<div style="text-align:center"><img src="img/blogpage/Simple_localisation.png" /></div>

We often come across to the scenarios for internationalization wherein we need to provide internationalization for different business cases.

For eg - A React app needs internationalization for two business types - school, college.
The application contains a form component for which the feild names for school and college are different.

This kind of problem arises when you have to provide 10 languages support for the application and the locale entries vary for each business type.

How to add the locale data for each business type ?
What to do when providing internationalization for same component for different languages along with the business types?


So here's the step by step solution

# Getting Started

## Step 1

Create a react app and install **react-intl** [![NPM](https://img.shields.io/npm/v/react-select.svg)](https://www.npmjs.com/package/react-intl)  as we will be using it internationalize our React app. 

``` bash 
$create-react-app react-internationalization 
```

``` bash 
$npm install --save react-intl
```

## Step 2

Wrap your app container with `IntlProvider`

<div style="text-align:center"><img src="img/blogpage/image1.png" /></div>

## Step 3

Maintain the folder structure as follows

![IntlProvider Step 3](img/blogpage/image2.png)

## Step 4

 We have to load the locale data for languages we want to support. This data is provided by `react-intl`. The locale data is added by calling `addLocaleData()`.
 As for now, we are focused on providing the language support to 2 different business types,hence we would be maintaining 2 resource folders for our corresponding business types and locales for English language so the translations of our custom text messages will be included in these files:
 

- \src\languages\resources_school\en-US.js

<div style="text-align:center"><img src="img/blogpage/image3.png" /></div>

- \src\languages\resources_college\en-US.js
   
<div style="text-align:center"><img src="img/blogpage/image4.png" /></div>

- \src\languages\index.js

<div style="text-align:center"><img src="img/blogpage/image5.png" /></div>

## Step 5

In `\src\languages\IntlUtils.js` we will develop a language provider helper component used to display localised strings using the `FormattedMessage` of react-intl.

<div style="text-align:center"><img src="img/blogpage/image8.png" /></div>

## Step 6

Now, finally using these added locales with your `IntlProvider` in `App.js` looks like

<div style="text-align:center"><img src="img/blogpage/image9.png" /></div>

and using the custom text from it as

<div style="text-align:center"><img src="img/blogpage/image10.png" /></div>

you can also use our language provider helper component i.e `IntlUtil` as

 ```js
<IntlUtils id="heading" defaultMessage="Internationalize React app"/>
```
Hence for languages other than "en" the translation messages are undefined and react-intl will display the defaultText.

## Step 7

Eventually, you can add the custom resources for other preferred languages for react app and add into the locale data using `addLocaleData()`. The current Locale for the app can changed as per user requirement.

Lets take a look to the output for the above scenario!

<div style="text-align:center"><img src="img/blogpage/image6.png" /></div>
<div style="text-align:center"><img src="img/blogpage/image7.png" /></div>

If you are looking for source code, you can find it *[here](https://github.com/snehalPatil-Sonawane/react-localization-intl)*.


**Thanks for reading!**
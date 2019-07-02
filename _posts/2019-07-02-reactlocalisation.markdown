---
title:  "React Localisation!"
subtitle: "Use React localisation corresponding to various business types"
author: "Snehal Patil"
avatar: "img/authors/snehal.JPEG"
image: "img/react.png"
date:   2019-07-02
---


We often come across to the scenarios for localization wherein we need to provide localization for different business cases.

For eg - A React app needs localization for two business types - school, college.
The application contains a form component for which the feild names for school and college are different.

This kind of problem arises when you have to provide 10 languages support for the application and the locale entries vary for each business type.

How to add the locale data for each business type ?
What to do when providing localization for same component for different languages along with the business types?


So here's the step by step solution

## Getting Started

**Step 1**

Create a react app using and install 

``` bash 
$create-react-app react-localization 
```

``` bash 
$npm i react-intl
```

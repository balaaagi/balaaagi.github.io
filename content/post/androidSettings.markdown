---
layout: post
title: Android Settings Menu - Learning
date: 2016-01-15 00:32:41.000000000 +05:30
type: androidlogs
date: 2016-01-15T00:00:00-00:00
draft: false
---

Making step by step progress over the [SunShine](https://github.com/balaaagi/SunShine) app.

This learn log covers how settings menu was added.

After listing the climate details from API using URL,URI and ASyncTask next step was to open new activity on clicking a list item.

It can be achieved using `setOnItemClickListener` of the ListView

To get the list item details use `getItem(index)` where index is the parameter of `onItemClick` overrided function. 


###Opening New Acitivity
New activity can be opened using `Intents`.

```java
Intent <intentName>=new Intent(<context>,<NewActivityclassName>.class);
startActivity(<intentName>);

```
To pass the details to the intent

`intentName.putExtra(<keyname>,value)`

###Settings Menu

To add a new settings menu

* Add new layout under menu folder
* Use tags `<menu>` and `<item>` tags
* Since this is usually a fragment inflate it under the method `onCreateOptionsMenu`
* To add actions to the clicking of settings use function `onOptionsItemSelected`
* Getitemid and based on conditions open further activities

####Settings activity

* Create a settings activity which extends `PreferenceActivity`
* OnPreferenceChange method is used for binding the values
* The settings acitivity can be opened using `addPreferenceFromResource`
* The layout can be designed under `xml` folder using various options elements





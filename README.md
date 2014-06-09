ngiStorage
==========

An Angular Stupid Simple web localStorage Service with simple/string, bool and obj handling. Currently, localStorage in browsers only stores string values. I needed a simple interface for a Cordova based app that stored boolean values to check and set toggles when my application started. I've thought about writing this having only one getter/setter that does the type conversion for you, but I just wanted to get this written in a few minutes.

* include localstorage-service.js in your html or index page

* Replace 'myApp' with your Angular app name, in localstorage-service.js
    angular.module('myApp').factory('$localStorage',function() {

* inject $localStorage wherever you need it in your angular app
    ('MainCtrl', function($scope,$http,$localStorage) {

Usage: Getters and Setters
-------------

I went with getters and setters in my ngApp to be explicit in the storage type so when someone gets a non-string variable they don't have to do type conversion. 

    $localStorage.setVariable(key,value)
    $localStorage.getVariable(key)
    
    $localStorage.setObject(key,value)
    $localStorage.getObject(key)

    $localStorage.setBool(key,value)
    $localStorage.getBool(key)
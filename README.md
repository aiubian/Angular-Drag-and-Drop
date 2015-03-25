# Angular-Drag-and-Drop

[AngularJS](http://angularjs.org/) directive for drag and drop.This directive can drag and drop in the child level too whatever the depth of the child is.

# How to use it

Data List 

    $scope.data = [
        { name: "Anik Islam", age: 22, gender: "Male" },
        { name: "Mofijul Islam", age: 21, gender: "Male" },
        { name: "Tanveer Islam", age: 24, gender: "Male" },
        { name: "Arifa Akter", age: 22, gender: "Female" },
        { name: "Shayla Islam", age: 22, gender: "Female" }

    ];

Add ```drag-drop``` atrribute in your table 

```
 <tr ng-repeat="user in data" drag-drop>
     <td>{{user.name}}</td>
     <td>{{user.age}}</td>
     <td>{{user.gender}}</td>
  </tr>
```
This only change data visually.

If you want to change property during drag and drop then bind property names by comma(,) wtih ```drag-drop``` attribute

```
 <tr ng-repeat="user in data" drag-drop="age,gender">
     <td>{{user.name}}</td>
     <td>{{user.age}}</td>
     <td>{{user.gender}}</td>
  </tr>
```
If you wanna to catch drop event

Declare e function in your controller
```
$scope.ondrop = function (e) {
        console.log(e);
}
```
Then bind this function with ```after-drop``` attribute

```
<tr ng-repeat="user in dataWithProperty" drag-drop="{{properties}}" after-drop="ondrop">
 ```
 
 
Chek Demo here in [Plunkr](http://plnkr.co/edit/1qZcq3)


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/anik123/angular-drag-and-drop/trend.png)](https://bitdeli.com/free "Bitdeli Badge")


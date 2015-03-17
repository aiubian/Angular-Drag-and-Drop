# Angular-Drag-and-Drop

[AngularJS](http://angularjs.org/) directive for drag and drop.This directive can drag and drop in the child level too whever the depth of the child is.

# How to use it

Add ```drag-drop``` atrributes in your table 

```
 <tr ng-repeat="user in data" drag-drop>
     <td>{{user.name}}</td>
     <td>{{user.age}}</td>
     <td>{{user.gender}}</td>
  </tr>
```
This only change data visually.

If you want to change property during drag and drop then bind property names wtih this ```drag-drop``` attributes

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
Then bind this function with this ```after-drop``` attribute

```
<tr ng-repeat="user in dataWithProperty" drag-drop="{{properties}}" after-drop="ondrop">
 ```
 
 
Chek Demo here in [Plunkr](http://plnkr.co/edit/1qZcq3)

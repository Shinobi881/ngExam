# ngExam
> An AngularJS 1.x exam from beginner to expert created by [@gdi2290](https://twitter.com/gdi2290)


1.  What's MVC architecture? – 
    a.  Application design pattern
    b.  Separation of concerns 
    c.  Model - Application data
    d.  View – Is how that data is represented in the 
    e.  Controller – Controls interactions between the two

2.  What's MVVM architecture? – 
    a.  $scope considered as the viewModel
    b.  There is still a model but the VM is what is directly representing data in the view

3.  What's two-way binding? – 
    a.  Immediate binding of view to viewModel (They will always see the same thing and update each other on change)

4.  What's ng-model? – 
    a.  Think of it as a way to filter data through an input.

5.  What is $http? – 
    a.  Angulars’ representation of XMLHTTPRequest
    b.  Returns a promise

6.  What is ng-repeat? – 
    a.   Like a map function that returns instances of custom HTML elements and gives a bunch of different methods for filtering and representing data passed through it (uses the $watchCollection service for tracking changes)
    b.  Works on both objects and arrays
    c.  Methods – filter, track by, order by, animations

7.  What are $index, $even, $odd, $first, and $last? 
    a.  $index get the number of the current iteration of ng-repeat
    b.  The rest, tells where an element lies in a collection (in relationship to their $index)

8.  How would you filter a list via ng-repeat?
    a.  ng-repeat=”num in [1, 2, 3, 4, 5] | filter:num % 2 === 0”

9.  What's the difference between angular.module('app' , []) and angular.module('app') – 
    a.  angular.module(‘app’, [])  - instantiates or overwrites a new angular module
    b.  angular.module(‘app’) – References a module called app¬

10. What are directives (briefly)? – 
    a.  Custom HTML elements 

11. Why would you use ng-submit instead of ng-click in some cases? – 
    a.  Attach a submit event to a form 

12. What's Dependency Injection? – 
    a.  Inject code that another piece of code relies on to run properly

13. Do other frameworks use dependency injection (even if only for internal use)? 
    - Answer: yes (React,Ember) - 

14. How would you inject services and what are the different ways to do so? – 
    a.  myApp.controller(‘Test’, [$scope, $watch, function($scope, $watch) { … }])
    b.  myApp.controller(‘Test’, function($scope, $watch) { … }]) (‘implicit’, use ng-annotate to deal with ‘strict mode issues’)
    c.  testController.$inject[$scope, $watch, testFactory]

15. What's jqLite? - https://goo.gl/12GKoQ - Stripped down version of jQuery

16. How do you ensure Angular uses jQuery when including them both? – 
    a.  Place it in the HTML header 
    b.  import/require it before angular

17. What are promises and how would you use them? – Lookup later - https://promisesaplus.com/ -
    a.  Ensure async operation of remote requests

18. What's the difference between factory/provider/service/value/constant? – 
    a.  Factory is just an object
    b.  Service is more of a constructor (in terms of proper usage)
    c.  Provider is a ‘service’ that can be passed into a .config to be used before everything else in the app loads
    d.  Value is just a simple service that returns a value
    e.  Constant is the same as a value but it can be used during the config phase

19. When would you use each one? - https://goo.gl/RhLZ6W

20. What are filters? – 
    a.  Methods of filtering data using binding or ng-model

21. Why would you use ng-src, ng-bind, and ng-cloak? – 
    a.  ng-src allows you to use “{{ url }}”,
    b.  ng-bind is another way of using {{ }}
    c.  ng-cloak waits for everything to load before putting it in the DOM 

22. What's the difference between ng-if and ng-show? – 
    a.  ng-if removes elements from the DOM they will be totally gone
    b.  ng-show/ng-hide – will disable or hide elements based on conditionals – and then sow them when appropriate https://goo.gl/RhLZ6W

23. What phases are there in angular? Answer: config -> bootstrap -> run
    a.  Config =>
    b.  Bootstrap => 
    c.  run

24. Why would you use .config() and .run() phase?
    a.  .config() – this is where app providers are setup
    b.  Executes after the injector is created only no more configing after the run

25. What is ng-app and how does angular bootstrap?
    a.  Directive for auto bootstrapping an angular app
    b.  Boostrap is initializing/starting your angular app

26. When would you use $q.all()? – 
    a.  Combines and resolves promises when their inputpromise is resolved

27. Where would you make your network calls controller, template, directive, or service and why? (where would you use $http) – 
    a.  From a service
    b.  You may want to use it elsewhere in your app and/or process the returned data before binding it to the view

28. Say that you are going to alert an error where would you put that alert from a network call? Service, controller, template and why????
 
29. How would you dynamically filter a list with an ng-repeat? – 
    a.  Use pipe and then a filter: ng-repeat=”item in items | filter:number” Can use multiple filters as well

30. What's ng-messages and ng-message?
    a.  Include angular-messages.js
    b.  Used for showing error messages conditionaly

31. What's ng-style and ng-class? 
    a.  Apply CSS styles conditionally

32. How would you attach something to the header of every http call?
    a.  $httpProvider.defaults.headers.[method goes here]
    b.  Do in the config phase

33. What is $scope.$on() and how would you use it?
    a.  Event listener on the local $scope object

34. What are $http interceptors?
    a.  Dfdfg???

35. What is "$locationChangeStart"? – 
    a.  What to do on the start of the applications url change
    b.  Background animation…
    c.  Method on the $location Provider service

36. What's html5Mode?-
    a.  Allows the browser to user regular urls instead of only hashed urls
    b.  Browsers that don’t support will default to hashbang

37. How do you turn off cache for a $http call?
    a.  $httpProvider.defaults.cache = false(default)
    b.  $httpProvider.defaults.cache = false(default)

38. What is the $templateCache?
    a.  Service Key, value store for getting and putting templates

39. How would you implement auth as in locking down certain parts of the app?
    a.  Oauth API or JWT

40. What's ui-router and why use it over ng-route?
    a.  Nested views and named views
    b.  ui-sref for linking named states
    c.  Pass information between states using $statePArams

41. What are states?
    a.  A specific representation of the application view

42. How do you resolve resources via state/route and how would you do so?
    a.  Add the ‘resolve’ object to a specific app state

43. Given 3 nested states, how would you load the most nested one after the root state resolves while allowing the middle state to load asynchronously?
    a.  ???

44. What types of directives are there? Angular: element, attribute, class (no one uses class)
    a.  Element
    b.  Attribute
    c.  class

45. What is $scope?
    a.  Object on controllers that binds data to the view

46. What is $rootScope?
    a.  The root of all $scope objects on all app controllers

47. What is "$destroy"?
    a.  Remove the current scope from it’s parents

48. What's one time binding?
    a.  Uses :: and won’t recalculate after the first digest

49. When and where would you normally use .$watch()?
    a.  Watching for changes on data $scope.$watch

50. What's a stateful filter vs a stateless filter?
    a.  Stateless - More like a pure function that filters
    b.  Stateful - Has dependencies that must get evaluated before executing 

51. What are .$dirty, .$pristine, .$valid, .$invalid, and .$submitted?
    a.  $dirty – A form has been dirtied with text
    b.  $pristine – A form that has not been dirtied
    c.  $valid/$invalid – Input validation
    d.  $submitted – Whether a form has been submitted

52. What's NgModelController?

53. What's FormController?

54. What's ng-model-options and why would you use it?

55. What are $validators and $asyncValidators?
    a.  For async server-side validation of forms

56. What's the difference between scope, $scope, and $rootScope?
    a.  scope for directives
    b.  $scope for dependencey injection

57. What's the difference between controller and link directives?
    a.  Controller for pre-compilation
    b.  Link for post-compilation
    c.  Use controller when you want to expose an API to other directives

58. How do you require a controller in a directive?
    a.  require: ‘^[controllerName]’

59. How do you require more than one controller in a directive?
    a.  require: [‘^HomeCtrl’, “ngModel]
    b.  

60. What's an isolated scope? 
    a.  Attaching a directive directly to a controller vs. to an entire module

61. For an isolate scope what are these symbols ?,@,=,&,* in relation to directives
    a.  

62. What are compile/pre-link/post-link phase for directives?

63. What is $interpolate?
    a.  Allows you to use the braces in angular

64. What is $compile?

65. What is $observe?

66. What's transclusion?

67. Why would you need transclusion?

68. What's bindToController: and controllerAs: syntax?
    a.  bindToController binds a directive to a controller
    b.  controllerAs allow you to alias a controllers name


69. What are directives and what are components?
    a.  Elements or attributes 
    b.  All of the pieces connected together, controller, service 

70. What's the difference between .$broadcast(), and .$emit()?

71. What are $timeout() and $interval() and how do you cancel them?

72. What's dirty checking?
    a.  $scope.$watch

73. Do other frameworks use dirty checking? Answer: yes (React,Polymer)

74. What is the .$digest() loop?
    a.  This is the “watcher of watchers”. It loops around all watchers and binding events and registers new changes to the events. In order to ‘force’ the event, you use $apply instead of $digest

75. What's the difference between .$digest() and .$apply()?
    a.  $apply is what the developer invokes to run the $digest loop

76. What are $watchGroup and $watchCollection?
    a.  $watchGroup takes an array of elements to watch 
    b.  $watchCollection is for watching actual arrays and objects

77. What are $eval, $parse and $evalAsync?
    a.  

78. What is $applyAsync?

79. What's a decorator in relation to angular's module system?
    a.  

80. How would you filter a large list with ng-repeat to include data from the server and client?

81. How would you grab the $injector/$scope from the chrome console?

82. Why is there ng-form?

83. How would you dynamically create forms?

84. What's CSP and how does it relate to angular?

85. How do you structure your files for a large team/project?

86. How would you use a module loader/bundler such as browserify, webpack, or systemjs with angular?

87. How would you asynchronously load angular?

88. How would you inject server rendered data into client angular?

89. What's a document fragment?

90. What's the ShadowDOM?

91. What is needed for your angular web app to work with JavaScript disabled?

92. What is needed for your angular web app to be rendered on the server to be sent down to the client?

93. Generally speaking how would you paraphrase angular?

94. How would you progressively enhance your RESTful app with a pub/sub?

95. How would you structure your app if you only had a realtime (pub/sub) API (no REST)?

96. What are the different ways to architect your angular app?
    a.  

97. What are the pros and cons of each design?

98. What are some anti patterns developers tend to fall into while using angular?
    a.  
99. What are the problems currently facing angular1?

100. Explain how Angular 2 is solving all of the problems from 1.x

101. Demonstrate a few ways to migrate an Angular 1 app to Angular 2

102. What's the difference between MVC, MVVM, MVP(SC), MVP(PV), PM, and how does it compare to Flux/Redux 
architecture?
___

enjoy — **AngularClass** 

<br><br>

[![AngularClass](https://cloud.githubusercontent.com/assets/1016365/9863770/cb0620fc-5af7-11e5-89df-d4b0b2cdfc43.png  "Angular Class")](https://angularclass.com)
##[AngularClass](https://angularclass.com)
> Learn AngularJS, Angular 2, and Modern Web Development form the best.
> Looking for corporate Angular training, want to host us, or Angular consulting? scott@angularclass.com

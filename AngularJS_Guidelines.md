# AngularJS Development Guidelines
### Purpose of this Guide
To introduce specific practices that can help improve performance, stability, legibility, maintainability, compliance, and end quality of AngularJS applications.
### More Guidelines Than Actual Rules
Universal adherence to these rules can be difficult or unadvisable. However, special attention should be paid to testing and assurance of the objectives listed above, when publishing code that violates the principles of this guide.
---
- Use `controllerAs` syntax instead of injecting `$scope` -- only inject `$scope` into controllers when needed e.g. when establishing watchers or listeners
- Avoid unnecessary dependency injections
- Avoid using `$rootScope` variables/events
- Avoid adding to the digest cycle
- Prefer `ng-bind` attribute over `{{}}`
- Use `ng-attr-x="{{vm.myVar}}"`, never `x={{vm.myVar}}`
- Use `ng-cloak` to prevent all remaining flashes of unresolved template
- Use `ng-strict-di` to introduce strict dependency checking
- Prefer `ng-if` over `ng-show`/`ng-hide`
- Avoid heavy controllers -- put as much logic in services as possible, especially network logic
- Use promises to get data from services
- Use constructor style for your controller names (e.g. `HomeController`)
- Lay out each file as an IIFE with the `use strict` prologue
- Avoid invoking expensive functions in template expressions -- these are reevaluated frequently
- Never use `$rootScope.$on` in a controller unless accompanied by a corresponding `$scope.$on('$destroy', myListener)`
- Pass scope variables (as well as all other volatile data) by value when building requests
- Use function hoisting and the `main` idiom to organize source
---
### Sources
- [John Papa Angular Styleguide](https://github.com/johnpapa/angular-styleguide)
- [AngularJS Docs](https://docs.angularjs.org/api)
# sportily-angular-fixture

A suite of AngularJS (1.x) directives for laying down Sportily fixtures, such as
self updating scores and timelines.

## Installation

Through bower: `bower install sportily-angular-fixture --save`

## Usage

Include `sportily.fixture.min.js` (and all its dependencies) in your application.

```html
<script src="components/moment/min/moment.min.js"></script>
<script src="components/angular-moment/angular-moment.min.js"></script>
<script src="components/lodash/dist/lodash.min.js"></script>
<script src="components/restangular/dist/restangular.min.js"></script>
<script src="components/sportily-angular-fixture/dist/js/sportily.fixture.min.js"></script>
```

Include `sportily.fixture.css` in your application.

```html
<link rel="stylesheet" href="components/sportily-angular-fixture/dist/css/sportily.fixture.css">
```

Add the module `sportily-fixture` as a dependency to your app module.

```js
var myapp = angular.module('myapp', ['sportily-fixture']);
```

Place a valid an access token into local storage. The directives will look here
for it automatically, and use it for all calls to the API.

```js
window.localStorage.setItem('access_token', '[YOUR-ACCESS-TOKEN]');
```

Wrap everything in the `sportily-fixture` directive, passing in the identifier
of the fixture to be displayed.

```html
<div ng-app="app" sportily-fixture="[FIXTURE-ID]">
    <!-- here you may use the `sportily-scores` and `sportily-timeline` directives. -->
</div>
```

### Scores

Inside of the `sportily-fixture` directive, use can display the current game
score using the `sportily-scores` directive, like so:

```html
<div ng-app="myapp" sportily-fixture="[FIXTURE-ID]">
    <sportily-scores></sportily-scores>
</div>
```

### Timeline

Inside of the `sportily-fixture` directive, use can display the current game
score using the `sportily-timeline` directive, like so:

```html
<div ng-app="myapp" sportily-fixture="[FIXTURE-ID]">
    <sportily-timeline></sportily-timeline>
</div>
```

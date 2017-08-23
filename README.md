# vue-skeleton (VueJS Cheatsheet)

VueJS skeleton app. Built with lessons gleaned from the [VueJS documentation](https://vuejs.org/v2/guide).


## Installation

Via npm:

```
npm install vue
```

Or bower:

```
bower install vue
```

## Application

A vue application is made up of the following parts. Usually, they are provided as an object with specific identifying keys/properties. 

For instance:

```javascript
var app = new Vue({
	el: '#app', //element
	data: {
		some_variable : 'some value'
	}
})
```

### Directives

*{{ some_var }}*

Mustache bars, displays the value of enclosed variable.

*v-bind*

Bind, ties a variable to some html element.

*v-if*

Tests a truth value.

*v-for*

*v-on*

*v-model*


### Element (el)

### Data (data)

### Methods (methods)

### Components

### Templates

### Props

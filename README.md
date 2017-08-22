# vue-skeleton (VueJS Cheatsheet)

VueJS skeleton app. Built with lessons gleaned from the [VueJS documentation](https://vuejs.org/v2/guide).


## Installation

Via npm:

```
npm install vue
```

Or nower:

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

### Element (el)

### Data (data)

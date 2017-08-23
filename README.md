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

## Directives

### {{ some_var }}

Mustache bars, displays the value of enclosed data variable.

```html
<span>{{ some_var }}</span>
```

### v-bind

Bind, ties a defined data variable to some html element.

```html
<span v-bind:title="some_var"></span>
```

### v-if

Toggles presence of an element based on a truth value of data.

```html
<span v-if="is_visible"></span>
```

### v-for

Loops. Works with data.

```html
<ul>
	<li v-for="single in list">{{ single.property }}</li>
</ul>
```

### v-on

Listens for an action and calls specificed method's function.

```html
<btn v-on:click="perform">Go!</btn>
```

### v-model

Two way binding especially form elements to data.

```html
<input v-model="some_var" />
```

## Application

A vue application is made up of the following parts. Usually, they are provided as an object with specific identifying keys/properties. 

For instance:

```javascript
var app = new Vue({
	//element
	el: '#app',
	//data
	data: {
		some_variable : 'some value'
	}
})
```

### Component

Well, a component is another Vue instance (a child one, if you will, with predefined parts/options. Among their important properties are props and template through which we specify arguments and html to output.

```javascript
Vue.component('component-name', {
	//props: arguments to be specified
	props: ['var1', 'var2'],
	//html to output
  	template: '<span>Firstname Surname</span>'
})
```

This then shows up in html as:

```html
<span title="Current User">
	<component-name v-bind:var1="value1" v-bind:var2="value2"></component-name>
</span>
```

### Element (el)

### Data (data)

### Methods (methods)

### Templates

### Props

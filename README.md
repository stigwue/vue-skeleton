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

Directives are special attributes with the *v-* prefix. Most are single javascript expressions and they can accept arguments.

### {{ some_var }}

Mustache bars, displays the value of enclosed data variable.

```html
<span>{{ some_var }}</span>
```

Note that mustache bars in the context of a *v-once* directive will not change as its variable changes.

### v-bind

Bind, ties a defined data variable to some html element.

```html
<span v-bind:title="some_var"></span>
```

Notice that binds go where mustache bars cannot (e.g HTML attributes).

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

### v-html

Replace content with raw html. Potentially dangerous.

```html
<div v-html="some_html_content"></div>
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

### Components

Well, a component is another Vue instance (a child one, if you will, with predefined parts/options. Among their important properties are props and template through which we specify arguments and html to output.

```javascript
Vue.component('cur-user', {
	//props: arguments to be specified
	props: ['first', 'last'],
	//html to output
  	template: '<span>{{ first }} {{ last }}</span>'
})
```

This then shows up in html as:

```html
<span title="Current User">
	<cur-user v-bind:first="Stephen" v-bind:last="Igwue"></cur-user>
</span>
```

### Filters

### Element (el)

### Data (data)

### Methods (methods)

### Templates

### Props

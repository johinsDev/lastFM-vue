# platzi-music

> App curso Vue.js de Platzi

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).
<template lang="pug">
  <div id="app">
    // // h1 {{ msg }}
    // // p {{ person.name.toUpperCase() }}
    // // pre {{ JSON.stringify(person) }}
    // // pre {{ $data }}
    // // p(v-show="showValue") {{ value }}
    // // p(v-if="showValue") {{ value }}
    // // p(v-else-if="!showValue") No
    // input(v-model="name")
    // button(@click="format") Format
    // input(v-model="lastName")
    // p {{ fullName }}

    // a(:href="url") Link
    // computed properties return variable
    // usan otros this.data
    // usado en funciones con interacciion constante con el dom
    // p {{ formatName  }}
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      // // msg: 'Hola Vue!',
      // // person: {
      // //   name: 'Johan'
      // // },
      // // showValue: false,
      // // value: 'Algo',
      // // name: 'johan',
      // // url: 'https://www.google.com'
      // name: '',
      // // lastName: '',
      // formatName: ''
    }
  },
  // methods: {
  //   format() {
  //     this.formatName = this.name.split(' ').join('-');
  //   }
  // }
  // computed: {
  //   fullName () {
  //     return `${this.name} ${this.lastName}`
  //   }
  // },
  // watch: {
  //   // llamada http cuando un input cambie
  //   // debe llevar el mismo nombre de la propiedad
  //   name(newValue, oldValue) {
  //     console.log(newValue, oldValue);
  //   }
  // }
}
</script>

<style lang="scss">
  @import './scss/main.scss'
</style>

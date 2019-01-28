# sandbox-nuxt

## 学び

```pug
.root
  input(type="text" :value="$props.value" @input="onInput")
</template>
```

```javascript
import Vue from "vue";
import { Component, Prop, Model, Emit } from "vue-property-decorator";

@Component({
  props: {
    value: String
  },
  model: {
    prop: 'value',
    event: 'input'
  }
})
class Input extends Vue {
  @Emit('input')
  onInput(event) {
    return event.target.value;
  }
}

export default Input;
```

```scss
//
```

> My remarkable Nuxt.js project

## Build Setup

``` bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn run dev

# build for production and launch server
$ yarn run build
$ yarn start

# generate static project
$ yarn run generate
```

For detailed explanation on how things work, checkout [Nuxt.js docs](https://nuxtjs.org).
# nuxt-sandbox-property-decorator

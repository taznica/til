# Install and enable bootstrap
Install bootstrap-vue in the project:

```
$ npm install --save bootstrap-vue
```

Register and import bootstrap-vue in main.js:

```main.js
import BootstrapVue from 'bootstrap-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

Vue.use(BootstrapVue)
```

Then main.js will be:

```main.js
import Vue from 'vue'
import App from './App'
import router from './router'

import BootstrapVue from 'bootstrap-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

Vue.use(BootstrapVue)

Vue.config.productionTip = false

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  components: { App },
  template: '<App/>'
})

```

---

If you separate entry point and component files, register bootstrap-vue in entry point(main.js):

```main.js
import BootstrapVue from 'bootstrap-vue'

Vue.use(BootstrapVue);
```

Then import css files in component file you want to enable bootstrap:

```.js
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
```

---

### References:
[Bootstrap-Vue Docs - Getting Started](https://bootstrap-vue.js.org/docs)

# Expense-tracker

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```


#Clear Asset, components and App.vue

#Create Own Component 

#write component template

#Import in App.Vue + Export and Register Components
```
<template>
  <Header />
</template>

<script>
    import Header from './components/Header.vue'

    export default {
      components: {
        Header,
      },
    }
</script>
```

# pass and Receive Props
```
 <TransactionList :transactions="transactions" />
```

```
import { defineProps } from 'vue'

    const props = defineProps({
        transactions:{
            type: Array,
            required: true,
        }
    })
```
# Tyoes of passing Props

- Pass as string
```
:transactions="transactions" 
```

- Pass as Number
```
:transactions="+transactions" 
```


# For MESSAGE NOTIFY

- STEP 1:  INSTALL PACKAGE
```
npm i vue-toastification@next
```

- STEP 2: ADD THESE IN MAIN.JS
```
import { createApp } from 'vue'
import Toast from 'vue-toastification'
import 'vue-toastification/dist/index.css'

import './assets/style.css'
import App from './App.vue'

const app = createApp(App)
app.use(Toast)
app.mount('#app')

```


# send from one componenet to app
- step 1: create emit
```
const emit = defineEmits('transactionSubmitted')
```

- step 2: create data and sent by emit
```
const transactionData = {
      text: text.value,
      amount: parseFloat(amount.value)
    }

    emit('transactionSubmitted', 'transactionData')
```


- npm run build
- cd dist
- git init
- git add .
- gti commit -m "msg"
- git remote add origin https://github.com/Muhammadtalha97/Expense-Tracker-in-VueJS
- git push -u origin master
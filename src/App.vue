<template>
  <div class="justify-center flex-1">
    <div class="container pt-8 mx-auto">
      <HelloWorld msg="Hello Vue 3 + Vite + Tailwind CSS" />
    </div>
  </div>
</template>

<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import * as Realm from 'realm-web'

const app: Realm.App = new Realm.App({ id: import.meta.env.VITE_REALM_APP_ID as string })
const credentials = Realm.Credentials.anonymous()
try {
  app
    .logIn(credentials)
    .then((user) => {
      console.log('user: ', user)
    })
    .catch((err) => {
      console.error('error logging in: ', err)
    })
} catch (err) {
  console.error('Failed to log in', err)
}
</script>

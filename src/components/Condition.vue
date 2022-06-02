<script setup>
import {ref} from "vue"
let a = false;

const user = ref({id: 0, name:"Hery", log:a})

function Connexion(){
 a = true
 console.log(a)
}

function Deconnexion(){
 a = false
 console.log(a)
}
</script>

<template>
<h1>CONDITION</h1>
<h2 v-if="user.log">Hello {{user.name}}</h2>
<h2 v-else>Hello Anonyme</h2>
<button v-if="user.log" @click="Deconnexion()">se déconnecter</button>
<button v-else @click="Connexion()">se connecter</button>
</template>
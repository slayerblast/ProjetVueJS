<script setup>
import {ref} from "vue"


const user = ref(null)

function Connexion(){
user.value = {id: 0, name:"Hery"}
 
}

function Deconnexion(){
user.value = null
}
</script>

<template>
<h1>CONDITION</h1>
<h2 v-if="user">Hello {{user.name}}</h2>
<h2 v-else>Hello Anonyme</h2>
<button v-if="user" @click="Deconnexion()">se déconnecter</button>
<button v-else @click="Connexion()">se connecter</button>
</template>
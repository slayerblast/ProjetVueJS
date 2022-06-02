<script setup>
import {ref} from "vue"

const tableau = ref([1,2,3])

const listObj = ref([
    {id: 0, name:"Alice"},
    {id: 1, name:"Alice"},
    {id: 2, name:"Alice"}
])
</script>
<template>
    <div>
    <p v-for="i in tableau"> {{i}} </p>
    <ul>
        <li v-for="monObjet in listObj" :key="monObjet.id" >{{monObjet}}</li>
    </ul>
    <div v-for="monObjet in listObj" :key="monObjet.id" >
    <h2>{{monObjet.name}} </h2>
    <p>{{monObjet.id}}</p>
    </div>
</div>

</template>
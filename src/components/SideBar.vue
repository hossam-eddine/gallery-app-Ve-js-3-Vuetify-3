<script setup>

import { defineEmits} from 'vue'



const emits=defineEmits(['selectOption'])


const selectop= (isColor) =>
{

    emits('selectOption',isColor)

}
</script>


<template>
    <v-navigation-drawer
    expand-on-hover
    rail
    >

    <v-list>
        <v-list-item 
        prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg"
        title="hossam edine"
        subtitle="clinix.me@gmail.com"
       
        >

        </v-list-item>
    </v-list>

<v-divider></v-divider>

<v-list density="compact" nav>

    <v-list-item prepend-icon="mdi-image" 
    title="Color Gallery"
    value="color"
    @click="selectop(true)"
>
</v-list-item>

<v-list-item prepend-icon="mdi-dialpad" 
title="GraySpace Effect"
value="gray"
@click="selectop(false)"
>
</v-list-item>


</v-list>



    </v-navigation-drawer>
</template>
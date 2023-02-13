<template>
    <v-layout>
      <v-navigation-drawer
        expand-on-hover
        rail
      >
      <v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Sandra Adams"
            subtitle="sandra_a88@gmailcom"
          ></v-list-item>
        </v-list>
        <v-divider></v-divider>
        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-image" title="Color Gallery" value="color" @click="ColorGallery()"></v-list-item>
          <v-list-item prepend-icon="mdi-dialpad" title="Grayspace Gallery" value="color" @click="GrayColor()"></v-list-item>
        </v-list>
      </v-navigation-drawer>

    </v-layout>

</template>
<script>
export default{
   data(){
     return{
        changeColor:''
     }
   },
   props:['changeColor'],
   methods:{
     ColorGallery(){
       alert('Hoo')
       this.changeColor = !this.changeColor
       
     },
     GrayColor(){
        alert('hello')
        this.changeColor = this.changeColor
     }
   }
}
</script>


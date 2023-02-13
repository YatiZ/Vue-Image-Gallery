<template>
    <v-card class="ma-5 pa-3 my-2">
    <v-row>
        <v-col
         v-for="n in 400"
         cols="4"
         sm="3"
         md="2"
         lg="1">
        <v-card @click="copyUrl">
            <v-img :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                   :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`" 
                aspect-ratio="1" cover>
                <template v-slot:placeholder>
                <v-row
                    class="fill-height ma-0"
                    align="center"
                    justify="center"
                >
                <v-progress-circular
                    indeterminate
                    color="red-lighten-5"
                ></v-progress-circular>
                </v-row>
                </template>
            </v-img>
                
        </v-card>
        </v-col>
    </v-row>
</v-card>
</template>
<script>
export default{
    props:['whichColor'],
    methods:{
        copyUrl(){
            this.copyUrl = async(url) =>{
                await navigator.clipboard.writeText(url)
            }
        }
    }
}

</script>

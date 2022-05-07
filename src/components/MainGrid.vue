<template>
    <section class="container">

        <app-loader v-if="loading" />

        <div class="row">
            <div class="col-6 col-md- 4 col-lg-3" v-for="(character) in characterList" :key="character.id" >
                <app-card :item= "character" />
            </div>
        </div>
        <app-footer :lunghezzaArray="characterList.length" v-if="!loading" />
        
<!-- 
        <div v-for="(item) in characterList" :key="item.id">
            id {{item.id}} - name {{name}} - status {{item.status}} - item {{item.type}} - species {{item.species}}
            <img :src="item.image" alt="">
        </div> -->
    
    </section>
</template>

<script>
import AppLoader from './AppLoader.vue'
import AppCard from './AppCard.vue'
import AppFooter from './AppFooter.vue'

import axios from 'axios';

export default {
    name: "MainGrid",
    components: {
        AppLoader,
        AppCard,
        AppFooter,
    },
    data(){
        return {
            characterList: [],
            apiPath : 'https://api.sampleapis.com/rickandmorty/',
            loading: false,
        }
    },
    mounted() {
        this.loading = true;
        axios.get(this.apiPath + 'characters').then((res)=> {
            console.log(res);
            this.characterList = res.data  // [...res.data]
            this.loading = false;
        }).catch((error)=> {
            console.log(error);
            this.loading = false;
        })
    }
}
</script>

<style lang="scss" scoped>

</style>
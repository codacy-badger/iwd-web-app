<template>
    <v-slide-y-reverse-transition>
        <v-container fluid v-show="show" class="">
            <v-layout wrap align-center justify-center row>
                <v-flex xs12 md10 lg10>
                    <attnedingHome/>
                    <attnedingExplore/>
                    <faq/>  
                </v-flex>
            </v-layout>
        </v-container>
    </v-slide-y-reverse-transition>
</template>

<script>

import faq from '@/components/faq'
import attnedingHome from '@/components/attending/attendingHome'
import attnedingExplore from '@/components/attending/attendingExplore'

export default {
    components:{
        faq,
        attnedingHome,
        attnedingExplore,
    },
    data() {
        return {
            show:false,
            imgPath:{
                src: require('@/assets/img/bg.jpg')
            }
        }
    },
    created(){
        this.show = true
    }
}
</script>

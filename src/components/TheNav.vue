<template>
    <v-app-bar
    flat
    :color="navColor"
    fixed
    >
        <!-- col que contiene el logo -->
            <v-img
            class="hidden-sm-and-down"
            src="@/assets/logo.png"
            width="12%"
            >
            </v-img>
            <v-btn
            color="transparent"
            class="display-sm-and-down hidden-md-and-up">
                <v-icon
                color="white">
                    mdi-menu
                </v-icon>
            </v-btn>
            <!-- col que contendrá las tabs para la navegación -->
            <v-tabs
            class="ml-9"
            :dark="Ontop"
            centered
            hide-slider
            background-color="transparent">
                <v-tab
                v-for="tab in tabs"
                :key="tab">
                    {{tab}}
                </v-tab>
            </v-tabs>
            <!-- col que contendrá la row de los botones -->
                <v-btn icon
                class="hidden-sm-and-down ml-5"
                v-for="icon in icons"
                :key="icon"
                >
                    <v-icon
                    
                    :color="Ontop ? 'white' : 'black'">
                        {{icon}}
                    </v-icon>
                </v-btn>
                <!-- Final row de botones -->
    </v-app-bar>
</template>

<script>
export default {
    data(){
        return{
            icons:['mdi-map-marker','mdi-account','mdi-cart','mdi-magnify','mdi-heart-outline'],
            tabs:['Lo nuevo','Ofertas','Muebles','Casas'],
            navColor:'transparent',
            Ontop:true
        };
    },
    mounted(){
        window.onscroll = () =>{
            this.cambiarColor();
        }
    },
    methods:{
        cambiarColor(){
            if(document.body.scrollTop > 100 || document.documentElement.scrollTop > 100)
            {
                this.navColor = '#ffffffb3';
                this.Ontop = false;
            } 
            else {
            this.navColor = 'transparent';
            this.Ontop = true;
            }
        }
    }

}
</script>

<style scoped>

</style>
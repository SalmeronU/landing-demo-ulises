<template>
    <div class="mainContainer">
        <v-row
        justify="center"
        >
            <h1>Lo más vendido</h1>
        </v-row>

        <div id="slider" class="slider d-flex">
                <v-col
                class="ma-0"
                lg="3"
                v-for="(area,index) in areaSections"
                :key="area.name"
                >
                    <v-card
                    height="100%"
                    :color="index%2 == 0 ? 'black' : 'darkGray'"
                    class="ma-0 cardSlider"
                >
                    <area-item :area="area"></area-item>
                    </v-card>
                </v-col>
        
        </div>
        
    </div>
</template>

<script>
import AreaItem from '../baseComponents/areaItem.vue'
export default {
    components:{AreaItem},
    props:['areaSections']
}
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
    .mainContainer{
        background-color: black;
    }

    .mainContainer h1{
        font-family: 'Montserrat', sans-serif;
        margin-top: 9vh;
        font-size: 4rem;
        color: white;
    }

    .cardSlider{
        padding-top: 12vh;
    }

    .slider{
        cursor:grabbing;
        overflow-x: auto;
        overflow-y: hidden;
    }




</style>
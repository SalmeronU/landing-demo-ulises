<template>
    <div class="itemContainer" style="text-align: center">
        <v-img
        v-if="area.name !='Dormitorios'"
        class="imgCard"
        width="80%"
        :src="area.img"
        >
        </v-img>

        <v-img
        v-else
        width="55%"
        class="imgCard"
        :src="area.img"
        >
        </v-img>
        

        <figcaption
        class="imgTag"
        >
            {{area.name}}
        </figcaption>

        <v-btn
        class="btnDescubrir">
            Descubrir
        </v-btn>
    </div>
</template>

<script>
export default {
    props:['area']
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
    .imgTag{
        font-family: 'Montserrat', sans-serif;
        text-align: center;
        font-size: 1.5rem;
        color: white;
        margin-top: 13vh;
    }

    .imgCard{
        margin: 8vh auto;
    }

    .itemContainer{
        padding-bottom: 4vh;
    }

</style>
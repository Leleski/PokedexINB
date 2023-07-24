<script setup>
const pokemon = defineProps(["name", "xp", "height", "img", "loading"])

</script>

<template>
              
    <div class="card cardPokemonSelected" :class="loading ? '' : 'animate__animated animate__flipInY'">
       <img v-if="pokemon.name" :src="pokemon.img" height="300" class="card-img-top pt-3" :alt="pokemon.name">

       <img v-else src="src/assets/egg_pokemon.svg" height="300" class="card-img-top pt-3" alt="???">

        <div class="card-body">
            <h5 class="card-title text-center">{{ pokemon.name || '???' }}</h5>
            <hr>
            <div class="row">
                <section class="col">
                    <strong>XP:</strong>
                    <span>{{ pokemon.xp }}</span>
                </section>
                
                <section class="col">
                    <strong>altura:</strong>
                    <span>{{ pokemon.height }}</span>
                </section>

            </div>
            <p class="card-text"></p>
       </div>           
    </div>        

</template>


<style scoped>
.cardPokemonSelected{
    height: 75vh;
    background: rgb(238,174,202);
    background: radial-gradient(circle, rgb(236, 140, 230) 0%, rgb(74, 139, 238) 100%);
    cursor: pointer;
}

</style>
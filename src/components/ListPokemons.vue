<script setup>
const pokemon = defineProps(["name","urlBaseSvg"])

</script>

<template>
    <div class="col-4">
        <div class="card p-2 mb-3 cardListPokemon">
            <p class="text-center">{{pokemon.name}}</p>
            <img :src="urlBaseSvg" class="card-img-top" alt="..."
            height="80"
            />

        </div>
    </div>
</template>

<style scoped>
.cardListPokemon{
    background: rgb(238,174,202);
    background: radial-gradient(circle, rgb(236, 140, 230) 0%, rgb(74, 139, 238) 100%);
    cursor: pointer;
}


.cardListPokemon:hover{
    background: rgb(238,174,202);
    background: radial-gradient(circle, rgb(236, 140, 230) 0%, rgb(74, 139, 238) 100%);
    cursor: pointer;
}


.cardListPokemon img:hover{
    padding: .2rem;
}

</style>
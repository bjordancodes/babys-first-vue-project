<template>
    <div>
    <h1 :key="ind" v-for="(bot, ind) in botArr"> {{botArr.name}}</h1>
    </div>
</template>


<script>
export default {
    props: {
        botArr: botArr
        }
    }
</script>


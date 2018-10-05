<template>
    <div>
    <form @submit.prevent="createBot(name, attack, health)">
    <h2>Name:</h2><input type="text" v-model="name"/><br/>
    <h2>Attack:</h2><input type="text" v-model="attack"/><br/>
    <h2>Health:</h2><input type="text" v-model="health"/><br/>
    <router-link to="/BotBattle"><button @click="createBot">Create my bot! </button></router-link>
    </form>
    <BotList :botArr="botArr"/>
    </div>
</template>
<script>
import BotList from '@/component/BotList.vue'
export default {
    data(){
        return {
            botArr: [
                {name: 'Metroid',
            attack: '100',
            health: '200'},
            {name: 'Allen',
            attack: '40',
            health: '201'},
            {name: 'Hilda',
            attack: '70',
            health: '300'}
            ],
            name: '',
            attack: '',
            health: ''
        }
    },
    methods: {
        createBot(){
            console.log(this.botArr)
            this.botArr.push({name: this.name,
            attack: this.attack,
            health: this.health});
            this.name = '',
            this.attack = '',
            this.health = ''
        }
    }
}
</script>


<style>

</style>


<template>
    <div id="root_ob">
        {{message}}
        <button @click="changed">Change</button>
    </div>
</template>

<script>
import Vue from 'vue'
    const state = Vue.observable({ message: 'Vue 2.6' })
    const mutation = {

        setMessage(value) {
            state.message = value
        }
    }
    export default {
        computed: {
            message() {
                return state.message
            }
        },
        methods: {
            changed() {
                mutation.setMessage('Vue 3.0')
            }
        }
    }

    
</script>

<style>

</style>
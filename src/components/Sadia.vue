<template>
    <div>
        <div v-html="name"></div>
        <form v-on:click.prevent="submitButton">
            <div>
                <input type="text" class="w-full" v-model="newToDo">
                <button>Submit</button>
            </div>
            <div v-if="error">
                {{error}}
            </div>

        </form>
    </div>
    <div v-for="(todo, index) in todos" v-bind:key="index">
        {{todo}}
    </div>
</template>

<script>
    export default {
        name: "Sadia",

        data() {
            return {
                name: '<h1>Form Submit</h1>',
                newToDo: '',
                todos: [],
                error:''
            }
        },
        methods: {
            submitButton() {
                if (this.newToDo !== '') {
                    this.todos.push(this.newToDo)
                } else {
                    this.error = 'This file in required'
                }

            }
        }
    }
</script>

<style scoped>

</style>
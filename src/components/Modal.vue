<template>
    <div v-if="isOpen" class="fixed inset-0 bg-gray-800 bg-opacity-75 flex items-center justify-center">
        <div class="max-w-md min-w- bg-white rounded shadow-2xl p-12 space-y-4">
            <div class="flex text-lg justify-between">
                <p>Login form</p>
            </div>
            <form @click.prevent="login">
                <div class="container mx-auto mb-3 block">
                    <label class="mb-3 block">
                        <input v-model="email" type="email"
                               class="w-full py-2 border rounded focus:outline-none px-4 focus:ring-2 focus:ring-pink-100"
                               placeholder="enter your email"/>
                        <span v-if="error.length > 0" class="text-red-600">{{error[0]}}</span>
                    </label>
                    <label>
                        <input v-model="password" type="password"
                               class="w-full py-2 border rounded focus:outline-none px-4 focus:ring-2 focus:ring-pink-100"
                               placeholder="Enter your password">
                        <span v-if="error.length > 0" class="text-red-600">{{error[1]}}</span>
                    </label>
                </div>
                <div class="flex space-x-4 pl-36">
                    <button class="py-3 px-5 text-lg font-medium leading-5 text-white rounded-lg bg-blue-400 hover:bg-blue-500">
                        Save
                    </button>
                    <button @click="close"
                            class="py-3 px-5 text-lg font-medium leading-5 text-white rounded-lg bg-red-400 hover:bg-blue-500">
                        Close
                    </button>
                </div>
            </form>
            <div v-for="(form,index) in forms" v-bind:key="index">
                {{form}}
            </div>
        </div>

    </div>
</template>

<script>
    export default {
        name: "Modal",
        props: ['isOpen'],
        data() {
            return {
                email: '',
                password: '',
                forms: [],
                error: []
            }
        },
        methods: {
            close() {
                this.$emit('close', this.isOpen)
            },
            login() {
                if (this.email === '') {
                    this.error.push('this filed id required');
                }
                if (this.password === '') {
                    this.error.push('this filed id required')
                }
                if (this.email !== '' && this.password !== '') {
                    this.forms.push(this.email);
                    this.forms.push(this.password);
                    this.error = '';
                }
            }
        },

    }
</script>

<style scoped>

</style>
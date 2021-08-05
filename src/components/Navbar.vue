<template>
    <div class="bg-black text-white py-5">
        <div class="container mx-auto flex justify-between">
            <div>
                <ul class="flex space-x-6">
                    <li class="flex items-center space-x-2">
                        <img src="../assets/bng.png" class="h-5 w-10 object-cover">
                        <span>  Bng </span>
                    </li>
                    <li>
                        +01628644184
                    </li>
                </ul>
            </div>
            <div>
                <ul class="flex space-x-6 font-medium">
                    <li v-for="(menu, index) in menus" v-bind:key="index">
                        {{menu}}
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Navbar",
        data(){
            return {
                menus: ['My Account','Wish list', 'Shopping', 'Cart','Checkout']
            }
        }
    }
</script>

<style scoped>

</style>
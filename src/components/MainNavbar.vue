<template>
    <div class="bg-white text-black py-2">
        <div class="container mx-auto justify-between">
            <div class="w-full flex items-center justify-start">
                <div class="w-1/5">
                    <Logo/>
                </div>
                <div class="w-2/5">
                    <ul class="flex space-x-6 text-xl font-mono justify-center uppercase">
                        <li class="italic" v-for="(item,index) in items" v-bind:key="index">
                            {{item}}
                        </li>
                    </ul>
                </div>

                <div class="w-2/5">
                    <div class="flex space-x-4 text-xl justify-end">
                        <div>
                            <Search></Search>
                        </div>
                        <div>
                            <WishList></WishList>
                        </div>
                        <div>
                            <Cart></Cart>
                        </div>
                        <div v-if="isAuth">
                            <span class="space-x-4">
                                Profile
                            </span>
                            <span>
                                Logout
                            </span>
                        </div>
                        <div v-else>
                            <login @click="modalOpen"></login>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </div>
    <Banner></Banner>
    <Body></Body>
    <Modal :isOpen="isOpen" @close="closeModal"></Modal>
</template>

<script>
    import Logo from "./Logo";
    import Login from "./Login";
    import Cart from "./Cart";
    import WishList from "./WishList";
    import Search from "./Search";
    import Banner from "./Banner";
    import Modal from "./Modal";
    import Body from "./Body";

    export default {
        name: "MainNavbar",
        components: {Body, Modal, Banner, Search, WishList, Cart, Login, Logo},

        data() {
            return {
                items: ['Home', 'Shop', 'About Us', 'Contact Us', 'Blog'],
                isAuth: false,
                isOpen: false
            }
        },
        methods: {
            modalOpen() {
                this.isOpen = true
            },
            closeModal() {
                this.isOpen = false;
            }
        },
    }
</script>

<style scoped>

</style>
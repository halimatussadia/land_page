<template>
    <div class="Container h-screen">
        <div class="main-section">
            <div class="section-1 bg-white justify-center items-center py-32">
                <div class="text-6xl font-medium px-96 italic">
                    <h1>Shop By Category</h1>
                </div>
                <div class="py-10">
                    <div class="profile-image flex space-x-6 justify-center">
                            <div class="photo-area h-auto flex relative">
                                <img class="object-contain" style="width: 400px;height: 300px;"
                                     src="https://preview.colorlib.com/theme/estore/assets/img/categori/cat1.jpg"
                                     alt="profile">
                                <div class="absolute top-16 left-72">
                                    <div class="py-3" >
                                        <p>Winter</p>
                                        <button class="right-2 mx-auto px-12 text-base font-medium leading-5 text-white rounded-full bg-blue-700 hover:bg-blue-800">
                                            Shop Now
                                        </button>
                                    </div>
                                    <div class="text-xl text-gray-600 italic py-2">
                                        <p>sellBest</p>
                                    </div>
                                </div>
                            </div>
                            <div class="photo-area">
                                <img class="object-contain" style="width: 400px;height: 300px;"
                                     src="https://preview.colorlib.com/theme/estore/assets/img/categori/cat2.jpg"
                                     alt="profile">
                            </div>
                            <div class="photo-area">
                                <img class="object-contain" style="width: 400px;height: 300px;"
                                     src="https://preview.colorlib.com/theme/estore/assets/img/categori/cat3.jpg"
                                     alt="profile">
                            </div>
                        </div>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Body"
    }
</script>

<style scoped>

</style>
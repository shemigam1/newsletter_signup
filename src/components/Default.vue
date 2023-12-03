
<template>
    <div id="main-container" class="relative min-w-full min-h-screen p-0 m-0 flex justify-center items-center bg-slate-700">
        <div class="container bg-white lg:w-2/3 w-full m-0 flex flex-col lg:flex-row lg:rounded-lg rounded-none">
            <div class="lg:p-3 lg:order-2">
                <img src="../assets/images/illustration-sign-up-desktop.svg" alt="">
            </div>
            <div class="mx-auto flex flex-col justify-between py-8 h-full my-10">

                <h1 class="text-5xl my-4 font-bold font-mono">Stay Updated!</h1>
                <p class="my-3">Join 10k product managers receivin monthly updates</p>
                <ul>
                    <li class="flex items-center my-3" v-for="list in listText">
                        <img src="../assets/images/icon-list.svg" alt="">
                        <p class="ml-4">{{ list }}</p>
                    </li>
                </ul>

                <!-- <form action=""> -->
                <div class="flex flex-col my-6">
                    <label for="email">Email Address</label>
                    <input class="h-11 border-slate-300 focus:border-slate-600 border p-4 rounded" type="text" name="email"
                        id="email" placeholder="example@mail.com">
                </div>
                <button class="border rounded bg-slate-800 hover:bg-red-600 text-white text-center h-12"
                    @click="transition">Subscribe to
                    monthly
                    newsletter</button>
                <!-- </form> -->
            </div>

        </div>
    </div>
</template>

<script setup>
const listText = ["Product discovery and building what matters", "Making shocking discoveries", "And so much more"]

const transition = () => {
    const main = document.getElementById('main-container')
    const thanks = document.getElementById("thanks-container")
    main.classList.toggle('hidden')
    thanks.classList.toggle('hidden')
}
</script>
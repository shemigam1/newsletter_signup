<template>
    <div id="thanks-container"
        class="relative min-w-full min-h-screen p-0 m-0 flex justify-center items-center lg:bg-slate-700 hidden">
        <div class="container bg-white lg:w-2/6 w-full m-0 flex flex-col lg:rounded-lg p-10">
            <div class="img">
                <img src="../assets/images/icon-success.svg" alt="">
            </div>
            <h1 class="text-5xl my-4 font-bold font-mono">Thanks for subscribing!</h1>
            <p class="my-3">A confirmation email has been sent to example@mail.com.
            </p>
            <button class="my-4 border rounded bg-slate-800 hover:bg-red-600 text-white text-center h-12"
                @click="transition">Dismiss
                Message</button>
        </div>
    </div>
</template>


<script setup>

const transition = () => {
    const main = document.getElementById('main-container')
    const thanks = document.getElementById("thanks-container")
    main.classList.toggle('hidden')
    thanks.classList.toggle('hidden')
}
</script>
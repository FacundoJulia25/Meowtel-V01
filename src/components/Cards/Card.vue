<template>
        <!-- GRID -->
        <div class=" border border-black rounded-lg bg-white m-2 flex flex-col" >
            <img class="w-auto h-80 object-cover" :src="img" :alt="name">
            <h1 class="text-center">{{ name }}</h1>
            <div class="text-center py-3 justify-around ">
                <h2 class="text-lg text-gray-600">{{ `Age: ` + age }}</h2>
                <h2 class="text-lg text-gray-600">{{ `Breed: ` + breed }}</h2>
            </div>
        </div>
        <!-- GRID -->
</template>

<script>
export default {
    props: ['name', 'age', 'img', 'breed'],
    data() {
        return {
        }
    }
}
</script>
//
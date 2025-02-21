<template>
    <main class="">
        <div class="overflow-x-hidden">
            <div class="text-center text-white">
                <h1 class="border p-2 rounded-2xl inline-flex text-xs mb-3">My Project</h1>
                <h1 class="text-3xl font-bold mb-30">Explore My Popular <span class="text-secondary">Project</span></h1>
            </div>
            <div class="md:flex block md:gap-40 justify-center items-center">
                <img src="../assets/img/Project1.png" class="w-170 h-110 rounded-2xl" alt="" data-aos="fade-right" data-aos-duration="1500" >
                <div class="text-white md:w-150 w-full text-justify" data-aos="fade-left" data-aos-duration="1500">
                    <h1 class="text-3xl font-bold mb-3">Project <span class="text-secondary">Figma</span></h1>
                    <h1 class="text-2xl mb-5">Design Bank</h1>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Optio quo consequuntur ullam eveniet aspernatur laborum cumque, quidem, doloribus molestias ex eligendi dignissimos rem animi impedit aliquam repellendus nesciunt tempore voluptatibus? Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores libero explicabo repellendus excepturi vel voluptatum molestias delectus quibusdam, odio velit recusandae laudantium facere earum vitae quidem fuga, atque, sunt ut!</p>
                    <button class="bg-secondary px-7 text-black rounded-lg mt-5 py-2">Figma</button>
                </div>
            </div>
            <div class="md:flex block md:gap-40 justify-center items-center mt-40 flex-row-reverse">
                <img src="../assets/img/Project2.png" class="w-170 h-110 rounded-2xl" alt=""  data-aos="fade-left" data-aos-duration="1500">
                <div class="text-white md:w-150 w-full text-justify" data-aos="fade-right" data-aos-duration="1500">
                    <h1 class="text-3xl font-bold mb-3">Project <span class="text-secondary">Figma</span></h1>
                    <h1 class="text-2xl mb-5">Design Coffee Shop</h1>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Optio quo consequuntur ullam eveniet aspernatur laborum cumque, quidem, doloribus molestias ex eligendi dignissimos rem animi impedit aliquam repellendus nesciunt tempore voluptatibus? Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores libero explicabo repellendus excepturi vel voluptatum molestias delectus quibusdam, odio velit recusandae laudantium facere earum vitae quidem fuga, atque, sunt ut!</p>
                    <button class="bg-secondary px-7 text-black rounded-lg mt-5 py-2">Figma</button>
                </div>
            </div>
            <div class="md:flex block md:gap-40 justify-center items-center mt-40">
                <img src="../assets/img/Project3.png" class="w-170 h-110 rounded-2xl" alt="" data-aos="fade-right" data-aos-duration="1500" >
                <div class="text-white md:w-150 w-full text-justify"  data-aos="fade-left" data-aos-duration="1500">
                    <h1 class="text-3xl font-bold mb-3">Project <span class="text-secondary">VUE</span></h1>
                    <h1 class="text-2xl mb-5">Admin Dashboard</h1>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Optio quo consequuntur ullam eveniet aspernatur laborum cumque, quidem, doloribus molestias ex eligendi dignissimos rem animi impedit aliquam repellendus nesciunt tempore voluptatibus? Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores libero explicabo repellendus excepturi vel voluptatum molestias delectus quibusdam, odio velit recusandae laudantium facere earum vitae quidem fuga, atque, sunt ut!</p>
                    <button class="bg-secondary px-7 text-black rounded-lg mt-5 py-2">VUE</button>
                </div>
            </div>
            <div class="md:flex block md:gap-40 flex-row-reverse justify-center items-center mt-40">
                <img src="../assets/img/Project4.png" class="w-170 h-110 rounded-2xl" alt="" data-aos="fade-left" data-aos-duration="1500">
                <div class="text-white w-full md:w-150 text-justify"    data-aos="fade-right" data-aos-duration="1500">
                    <h1 class="text-3xl font-bold mb-3">Project <span class="text-secondary">VUE</span></h1>
                    <h1 class="text-2xl mb-5">Admin Dashboard</h1>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Optio quo consequuntur ullam eveniet aspernatur laborum cumque, quidem, doloribus molestias ex eligendi dignissimos rem animi impedit aliquam repellendus nesciunt tempore voluptatibus? Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores libero explicabo repellendus excepturi vel voluptatum molestias delectus quibusdam, odio velit recusandae laudantium facere earum vitae quidem fuga, atque, sunt ut!</p>
                    <button class="bg-secondary px-7 text-black rounded-lg mt-5 py-2">VUE</button>
                </div>
            </div>
            <div class="flex justify-center mt-20">
                <button class="bg-secondary py-2 px-7 rounded-lg">Learn More</button>
            </div>
        </div>

    </main>

    <div class="mt-30">
        <Blog/>
    </div>
</template>

<script>
import Blog from '../views/Blog.vue'
export default {
    components: { Blog },
}

</script>
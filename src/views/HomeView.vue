<template>
  <div class="overflow-x-hidden">
    <main class="md:pt-80 md:mt-0 mt-50">
      <div
        class="md:flex md:justify-around md:items-center md:text-white bg-gray-10"
      >
        <div class="md:block hidden">
          <h1
            class="text-3xl font-light"
            data-aos="fade-right"
            data-aos-duration="1500"
          >
            Hello, i'm
          </h1>
          <h1
            class="text-5xl font-bold text-secondary"
            data-aos="fade-right"
            data-aos-duration="1500"
          >
            {{ displayedText }}
          </h1>
          <h1
            class="text-3xl font-light"
            data-aos="fade-right"
            data-aos-duration="1500"
          >
            UI/UX and Frontend Development
          </h1>
          <p
            class="md:w-100 font-extralight text-lg"
            data-aos="fade-right"
            data-aos-duration="1500"
          >
            Hai, nama saya Ilham Yuniar Tio Al Fahrozi bisa dipanggil ilham ini
            adalah portofolio saya
          </p>
          <div
            class="md:flex md:gap-10 mt-5"
            data-aos="fade-right"
            data-aos-duration="1500"
          >
            <button
              class="bg-secondary cursor-pointer p-3 rounded-lg pl-5 pr-5 text-black"
            >
              <a href="#about">Telusuri</a>
            </button>
            <button class="underline cursor-pointer" @click="gotogithub">Github --></button>
          </div>
        </div>
        <div
          class="md:mr-40 flex justify-center items-center md:w-100 w-full flex-col gap-10"
        >
          <img
            src="../assets/img/img2.avif"
            class="md:w-100 md:h-100 w-50 h-50 rounded-full object-cover"
            alt=""
            data-aos="fade-down"
            data-aos-duration="1500"
          />
          <div class="md:hidden text-center text-white">
            <h1 class="text-3xl font-light">Hello, i'm</h1>
            <h1 class="text-5xl font-bold text-secondary">{{ displayedText }}</h1>
            <h1 class="text-2xl font-light">UI/UX and Frontend Development</h1>
            <p class="md:w-100 w-full font-extralight text-xs">
              Hai, nama saya Ilham Yuniar Tio Al Fahrozi bisa dipanggil ilham ini
              adalah portofolio saya
            </p>
            <div class="justify-center flex gap-10 mt-5">
              <button
                class="bg-secondary cursor-pointer p-3 rounded-lg pl-5 pr-5 text-black"
              >
                Telusuri
              </button>
              <button class="underline cursor-pointer" @click="gotogithub">Github --></button>
            </div>
          </div>
        </div>
  
        <!-- Konten Utama -->
  
        <main data-aos="fade-left">
          <div
            v-for="(item, index) in items"
            :key="index"
            class="md:w-37 w-full mt-40 md:mt-0 md:mr-40 md:block text-white"
          >
            <div
              v-if="openUtama === index"
              class="flex justify-between md:block bg-black rounded-2xl"
              data-aos="fade-left"
              data-aos-easing="ease-in-out"
            >
              <div
                class="flex flex-col text-2xl md:border-b md:border-b-gray-600 border-r md:border-r-0 p-5 pt-10 pb-10"
              >
                <span class="text-secondary font-bold text-4xl">{{
                  item.jml
                }}</span>
                <span class="text-xs">{{ item.judul1 }}</span>
              </div>
              <div
                class="flex flex-col text-2xl md:border-b p-5 md:border-b-gray-600 border-r md:border-r-0 pt-10 pb-10"
              >
                <span class="text-secondary font-bold text-4xl">{{
                  item.jml1
                }}</span>
                <span class="text-xs">{{ item.judul2 }}</span>
              </div>
              <div class="flex flex-col text-2xl p-5 rounded-b-2xl pt-10 pb-10">
                <span class="text-secondary font-bold text-4xl">{{
                  item.jml2
                }}</span>
                <span class="text-xs">{{ item.judul3 }}</span>
              </div>
            </div>
          </div>
        </main>
        <main
          class="absolute md:top-85 md:right-7 bg-black text-center rounded-2xl md:mt-0 mt-30 md:block top-160 flex justify-around md:w-16 w-full text-white overflow-hidden"
          data-aos="fade-left"
          data-aos-duration="1500"
        >
          <main v-for="(item, index) in items" :key="index" class="">
            <button
              @click="openUtamaModal(index)"
              class="md:mb-10 hover:bg-secondary p-5 rounded-2xl cursor-pointer"
            >
              <component :is="item.me" class="w-6 h-6" />
              <component :is="item.me1" class="w-6 h-6" />
              <component :is="item.me2" class="w-6 h-6" />
              <component :is="item.me3" class="w-6 h-6" />
            </button>
          </main>
        </main>
      </div>
    </main>
    <div class="md:absolute top-0 md:left-460 -z-10 -translate-x-1/2 blur-3xl xl:-top-6" aria-hidden="true">
        <div class="md:aspect-1155/678 md:w-[72.1875rem] bg-linear-to-tr from-[#ff80b5] to-[#9089fc] opacity-30" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
      </div>
  </div>

  <div id="about" class="md:mt-75">
    <AboutPage />
  </div>
</template>

<script>
// import { RouterLink } from "vue-router";
import AboutPage from "./AboutView.vue";
import {
  HomeIcon,
  CogIcon,
  BellIcon,
  FunnelIcon,
} from "@heroicons/vue/24/solid";
export default {
  components: { HomeIcon, CogIcon, BellIcon, FunnelIcon, AboutPage },
  data() {
    return {
      x: 0,
      y: 0,
      fullText: "Ilham Yuniar Tio",
      displayedText: "",
      index: 0,
      deleting: false,
      openUtama: null,
      items: [
        {
          jml: "5+",
          jml1: "4+",
          jml2: "5+",
          judul1: "Design Web",
          judul2: "Web Mobile",
          judul3: "Web Desktop",
          me: "HomeIcon",
        },
        {
          jml: "2+",
          jml1: "3+",
          jml2: "5+",
          judul1: "Sertifikat Bootcamp",
          judul2: "Sertifikat Lomba",
          judul3: "Sertifikat Seminar",
          me1: "CogIcon",
        },
        {
          jml: "1",
          jml1: "5+",
          jml2: "4+",
          judul1: "Sertifikat Analisis",
          judul2: "UI/UX Design",
          judul3: "Sertifikat Magang",
          me2: "BellIcon",
        },
        {
          jml: "5+",
          jml1: "4+",
          jml2: "5+",
          judul1: "Design Web",
          judul2: "Web Mobile",
          judul3: "Web Desktop",
          me3: "FunnelIcon",
        },
      ],
    };
  },
  mounted() {
    this.startTypingEffect();
    window.addEventListener('mousemove', this.handleMouseMove);
  },
  beforeMount() {
    window.removeEventListener('mousemove', this.handleMouseMove);
  },
  methods: {
    gotogithub() {
      window.location.href = 'https://github.com/Lynxx16-06';
    },
    handltheMouseMove(event) {
      this.x = event.clientX;
      this.y = event.clientY;
    },

    startTypingEffect() {
      const typingInterval = setInterval(() => {
        if (!this.deleting && this.index < this.fullText.length) {
          this.displayedText += this.fullText[this.index];
          this.index++;
        } else if (this.deleting && this.index > 0) {
          this.index--;
          this.displayedText = this.fullText.substring(0, this.index);
        } else {
          this.deleting = !this.deleting;
          setTimeout(() => {});
        }
      }, 200);
    },
    openUtamaModal(index) {
      this.openUtama === index ? (this.openUtama = null) : (this.openUtama = index);
    },
  },
};
</script>

<style>
@keyframes blink {
  50% {
    opacity: 0;
  }
}

.animate-blink {
  animation: blink 0.8s infinite;
}

.cursor {
  mix-blend-mode: difference;
}
</style>

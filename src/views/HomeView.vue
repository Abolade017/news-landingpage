<script setup>
const news = [
  {
    id: 1,
    title: "Hydrogen Vs Electric cars",
    description: "Will hydrogen-fueled car ever catch up to EVs?",
    style: "border-b border-b-neutral-grayish-blue",
  },
  {
    id: 2,
    title: "The Downside of Al Artistry",
    description:
      "What are the possible adverse efffects on-demand Al image generation?",
    style: "border-b border-b-neutral-grayish-blue",
  },
  {
    id: 3,
    title: "Is VC Funding Drying Up",
    description:
      "Private funding by vc firm is down is 50% YOY. We take a look at what that means.",
    style: "",
  },
];
const trends = [
  {
    id: "01",
    title: "Reviving Retro Pcs",
    description: "What happens when old PCs are given modern upgrades?",
    picture: "image-retro-pcs.jpg",
  },
  {
    id: "02",
    title: "Top 10 Laptops of 2022",
    description: "Our best picks of various needs and budgets.",
    picture: "image-top-laptops.jpg",
  },
  {
    id: "03",
    title: "The Growth of Gaming",
    description: "How the pandemics has sparked fresh opportunities.",
    picture: "image-gaming-growth.jpg",
  },
];
</script>

<template>
  <main class="px-4 md:px-0">
    <div class="flex flex-col md:flex-row md:space-x-12 space-x-0">
      <div class="w-full md:w-2/3">
        <img src="/images/image-web-3-desktop.jpg" alt="desktop image" />
        <div class="flex flex-col md:flex-row space-x-0 md:space-x-40 mt-10">
          <div class="w-full md:w-1/2">
            <h1 class="text-6xl text-neutral-very-dark-blue font-bold">
              The Bright Future of Web 3.0?
            </h1>
          </div>
          <div class="w-full md:w-1/2 mt-4 md:mt-0">
            <p
              class="text-[17px] md:text-[15px] text-neutral-dark-grayish-blue"
            >
              We dive into the next evolution of the web that claims to put the
              power of the platforms back into the hands of the people. But it
              is really fulfilling its promise?
            </p>
            <div class="mt-8">
              <button
                class="font-bold h-12 w-56 uppercase text-white bg-primary-soft-red px-12 my-2"
              >
                Read More
              </button>
            </div>
          </div>
        </div>
      </div>
      <div class="w-full md:w-1/3 bg-neutral-very-dark-blue mt-12 md:mt-0">
        <h2
          class="px-10 py-4 md:py-10 text-primary-soft-orange text-4xl font-bold"
        >
          New
        </h2>
        <div class="px-10 grid gap-y-6">
          <div class="" v-for="info in news" :key="info.id" :class="info.style">
            <div class="pb-6">
              <h3
                class="capitalize text-neutral-off-white text-xl font-bold py-2"
              >
                {{ info.title }}
              </h3>
              <p class="text-neutral-grayish-blue leading-7">
                {{ info.description }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="flex md:flex-row flex-col space-x-0 md:space-x-10 md:space-y-0 space-y-6 pt-14 md:pt-20 pb-40"
    >
      <div class="w-full md:w-1/3" v-for="trend in trends">
        <div class="flex space-x-6 md:space-x-8">
          <!-- <div class="w-36 h-36 bg-green-500"> -->
          <img
            :src="'/images/' + trend.picture"
            alt="trends picture"
            class="h-32 w-24 object-cover md:w-40"
          />
          <!-- </div> -->
          <div class="flex flex-col space-y-2">
            <div class="text-2xl text-neutral-grayish-blue font-bold">
              {{ trend.id }}
            </div>
            <div class="font-bold text-neutral-very-dark-blue text-xl">
              {{ trend.title }}
            </div>
            <div class="text-neutral-dark-grayish-blue">
              {{ trend.description }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

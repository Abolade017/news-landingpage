<script setup>
import { RouterLink, RouterView } from "vue-router";
import {
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  Menu,
  MenuButton,
  MenuItem,
  MenuItems,
} from "@headlessui/vue";
import { Bars3Icon, BellIcon, XMarkIcon } from "@heroicons/vue/24/outline";
</script>

<template>
  <!-- <div class="max-w-7xl mx-auto">
    <header class="mt-24 mb-14">
      <div class="hidden md:flex justify-between items-center">
        <div>
          <img
            alt="news logo"
            class="logo"
            src="/images/logo.svg"
            width="80"
            height="80"
          />
        </div>
        <div class="wrapper">
          <nav>
            <div class="flex space-x-12 text-neutral-grayish-blue">
              <RouterLink to="/">Home</RouterLink>
              <RouterLink to="/about">News</RouterLink>
              <RouterLink to="/about">Popular</RouterLink>
              <RouterLink to="/about">Trending</RouterLink>
              <RouterLink to="/about">Categoriess</RouterLink>
            </div>
          </nav>
        </div>
      </div>
    </header>

  </div> -->
  <div class="mx-auto max-w-7xl">
    <Disclosure
      as="nav"
      class="bg-white mt-8 sm:mt-24 mb-12 sm:mb-14"
      v-slot="{ open }"
    >
      <div class="flex h-16 justify-between px-4 sm:px-0">
        <div class="flex flex-shrink-0 items-center">
          <img
            alt="news logo"
            class="logo"
            src="/images/logo.svg"
            width="80"
            height="80"
          />
        </div>
        <div class="wrapper">
          <div class="hidden sm:flex space-x-12 text-neutral-grayish-blue">
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">News</RouterLink>
            <RouterLink to="/about">Popular</RouterLink>
            <RouterLink to="/about">Trending</RouterLink>
            <RouterLink to="/about">Categoriess</RouterLink>
          </div>
          <div class="flex items-center sm:hidden">
            <!-- Mobile menu button -->
            <DisclosureButton
              class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:text-gray-500 focus:outline-none"
            >
              <span class="absolute -inset-0.5" />
              <span class="sr-only">Open main menu</span>
              <Bars3Icon
                v-if="!open"
                class="block h-6 w-6 text-neutral-very-dark-blue"
                aria-hidden="true"
              />
              <XMarkIcon v-else class="block h-6 w-6" aria-hidden="true" />
            </DisclosureButton>
          </div>
        </div>
      </div>
      <DisclosurePanel class="sm:hidden">
        <div class="flex flex-col space-y-1 pb-3 pt-2">
          <!-- Current: "bg-indigo-50 border-indigo-500 text-indigo-700", Default: "border-transparent text-gray-500 hover:bg-gray-50 hover:border-gray-300 hover:text-gray-700" -->
          <RouterLink
            to="/"
            class="block border-l-4 border-primary-soft-orange text-neutral-grayish-blue py-2 pl-3 pr-4 text-base"
            >Home</RouterLink
          >
          <RouterLink
            to="/about"
            class="block border-l-4 text-neutral-grayish-blue py-2 pl-3 pr-4 text-base"
            >News</RouterLink
          >
          <RouterLink
            to="/about"
            class="block border-l-4 text-neutral-grayish-blue py-2 pl-3 pr-4 text-base"
            >Popular</RouterLink
          >
          <RouterLink
            to="/about"
            class="block border-l-4 text-neutral-grayish-blue py-2 pl-3 pr-4 text-base"
            >Trending</RouterLink
          >
          <RouterLink
            to="/about"
            class="block border-l-4 text-neutral-grayish-blue py-2 pl-3 pr-4 text-base"
            >Categoriess</RouterLink
          >
        </div>
      </DisclosurePanel>
    </Disclosure>
    <RouterView />
  </div>
</template>

<style scoped></style>

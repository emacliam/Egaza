<template>
  <main class="bg-white">
    <div
      class="fixed w-full h-16 shadow-lg border-b border-blue-300 bg-gray-100"
    >
      <div class="w-full h-16 mn flex items-center justify-between px-24">
        <div class="flex space-x-2 items-center">
          <img src="/chat.svg" alt="" class="w-10 h-10" />
          <a href="/home" class="text-orange-600 text-xl font-bold">Egaza</a>
        </div>
        <body class="relative">
          <div id="app" class="h-full w-full flex items-center justify-center">
            <transition name="fade">
              <div v-show="show_modal" class="fixed inset-0 z-30">
                <!--       background -->
                <div
                  v-show="show_modal"
                  @click="showModal()"
                  class="bg-filter bg-gray-600 opacity-25 fixed inset-0 w-full h-full z-20"
                ></div>
                <!--          -->
                <main
                  class="flex flex-col items-center justify-center h-full w-full"
                >
                  <transition name="fade-up-down">
                    <div
                      v-show="show_modal"
                      class="modal-wrapper inline-block flex items-center z-30 "
                    >
                      <div
                        class="modal max-w-md mx-auto xl:max-w-2xl lg:max-w-2xl md:max-w-md  max-h-screen flex-row  relative"
                      >
                        <div class="py-3 sm:max-w-xl sm:mx-auto">
                          <div
                            class="bg-white min-w-1xl flex flex-col rounded shadow-lg"
                          >
                            <div class="px-12 py-5">
                              <h2 class="text-gray-600 text-3xl font-semibold">
                                Create a Post
                              </h2>
                            </div>
                            <div class="w-full flex flex-col items-center">
                              <div class="">
                                <label class="block text-sm" for="name"
                                  >name</label
                                >
                                <input
                                  class="w-full px-5 py-1 text-gray-700 bg-gray-300 rounded-lg focus:outline-none focus:bg-white focus:border focus:border-purple-300 border border-white"
                                  type="name"
                                  id="name"
                                  placeholder="Enter your name"
                                  aria-label="name"
                                  required
                                  v-model="name"
                                />
                              </div>
                              <div class="">
                                <label class="block text-sm" for="name"
                                  >name</label
                                >
                                <input
                                  class="w-full px-5 py-1 text-gray-700 bg-gray-300 rounded-lg focus:outline-none focus:bg-white focus:border focus:border-purple-300 border border-white"
                                  type="name"
                                  id="name"
                                  placeholder="Enter your name"
                                  aria-label="name"
                                  required
                                  v-model="name"
                                />
                              </div>
                              <div class="">
                                <label class="block text-sm" for="name"
                                  >name</label
                                >
                                <input
                                  class="w-full px-5 py-1 text-gray-700 bg-gray-300 rounded-lg focus:outline-none focus:bg-white focus:border focus:border-purple-300 border border-white"
                                  type="name"
                                  id="name"
                                  placeholder="Enter your name"
                                  aria-label="name"
                                  required
                                  v-model="name"
                                />
                              </div>
                              <div class="">
                                <label class="block text-sm" for="name"
                                  >name</label
                                >
                                <input
                                  class="w-full px-5 py-1 text-gray-700 bg-gray-300 rounded-lg focus:outline-none focus:bg-white focus:border focus:border-purple-300 border border-white"
                                  type="name"
                                  id="name"
                                  placeholder="Enter your name"
                                  aria-label="name"
                                  required
                                  v-model="name"
                                />
                              </div>
                              <div class="p-4">
                                <label class="block text-sm" for="text"
                                  >Text</label
                                >
                                <textarea
                                  class="w-full px-5 py-1 text-gray-700 bg-gray-300 rounded-lg focus:outline-none focus:bg-white focus:border focus:border-purple-300 border border-white"
                                  type="text"
                                  id="text"
                                  placeholder="Enter your text"
                                  aria-label="text"
                                  required
                                  name=""
                                  cols="20"
                                  rows="4"
                                  v-model="text"
                                ></textarea>
                              </div>
                              <div class="w-3/4 flex flex-col">
                                <button
                                  @click="send()"
                                  class="py-1 my-2 text-lg bg-blue-700 rounded text-white"
                                >
                                  Create
                                </button>
                              </div>
                            </div>
                            <div class="h-20 flex items-center justify-center">
                              <button
                                @click="showModal()"
                                class="text-blue-600"
                              >
                                Maybe later
                              </button>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </transition>
                </main>
              </div>
            </transition>
          </div>
        </body>

        <!-- component -->
        <div class="relative text-gray-400">
          <input
            type="search"
            name="serch"
            placeholder="Search"
            class="bg-white h-8 px-5 pr-10 rounded-full text-sm focus:outline-none border hover:shadow focus:shadow"
          />
          <button type="submit" class="absolute right-0 top-0 mt-2 mr-4">
            <svg
              class="h-4 w-4 fill-current"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              version="1.1"
              id="Capa_1"
              x="0px"
              y="0px"
              viewBox="0 0 56.966 56.966"
              style="enable-background:new 0 0 56.966 56.966;"
              xml:space="preserve"
              width="512px"
              height="512px"
            >
              <path
                d="M55.146,51.887L41.588,37.786c3.486-4.144,5.396-9.358,5.396-14.786c0-12.682-10.318-23-23-23s-23,10.318-23,23  s10.318,23,23,23c4.761,0,9.298-1.436,13.177-4.162l13.661,14.208c0.571,0.593,1.339,0.92,2.162,0.92  c0.779,0,1.518-0.297,2.079-0.837C56.255,54.982,56.293,53.08,55.146,51.887z M23.984,6c9.374,0,17,7.626,17,17s-7.626,17-17,17  s-17-7.626-17-17S14.61,6,23.984,6z"
              />
            </svg>
          </button>
        </div>
        <!--
        <div class="flex items-center ">
          <div class="" @click="isVisible = false"></div>
          <div
            class="relative inline-block"
            @mouseover="isVisible = true"
            @mouseleave="isVisible = false"
            @keydown.enter="isVisible = !isVisible"
          >
            <button
              type="button"
              class="inline-flex items-center justify-between px-2 py-1 font-medium text-gray-700 transition-all duration-500 rounded-md"
            >
              <svg
                fill="currentColor"
                viewBox="0 0 20 20"
                class="flex-shrink-0 w-5 h-5 ml-1 text-purple-600"
              >
                <path
                  :class="{ 'rotate-180': isVisible }"
                  class="transition duration-300 ease-in-out origin-center transform"
                  fill-rule="evenodd"
                  d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                  clip-rule="evenodd"
                ></path>
              </svg>
            </button>
            <transition
              enter-active-class="transition duration-300 ease-out transform"
              enter-class="-translate-y-3 scale-95 opacity-0"
              enter-to-class="translate-y-0 scale-100 opacity-100"
              leave-active-class="transition duration-150 ease-in transform"
              leave-class="translate-y-0 opacity-100"
              leave-to-class="-translate-y-3 opacity-0"
            >
              <div v-show="isVisible" class="absolute pt-2">
                <div
                  class="relative py-1 bg-white border border-gray-200 rounded-md shadow-xl"
                >
                  <div
                    class="absolute top-0 w-4 h-4 origin-center transform rotate-45 translate-x-16 -translate-y-2 bg-white border-t border-l border-gray-200 rounded-sm pointer-events-none"
                  ></div>
                  <div class="relative">
                    <a
                      href="/profile"
                      class="underline block w-full px-4 py-2 font-medium text-gray-700 whitespace-no-wrap hover:bg-purple-300 focus:outline-none hover:text-gray-900 focus:text-gray-900 focus:shadow-outline transition duration-300 ease-in-out"
                    ></a>
                    <hr />
                    <a
                      class=" text-center block w-full px-4 py-2 font-medium text-gray-700 whitespace-no-wrap hover:bg-purple-300 focus:outline-none hover:text-gray-900 focus:text-gray-900 focus:shadow-outline transition duration-300 ease-in-out"
                      >Logout</a
                    >
                  </div>
                </div>
              </div>
            </transition>
          </div>
        </div> -->
        <div class="flex w-auto flex space-x-4">
          <a
            href="/login"
            class="border border-gray-300 hover:border-gray-600 py-1 px-4 rounded"
            >Login</a
          >
          <a
            href="/signup"
            class=" py-1 px-4  rounded bg-blue-600 text-white hover:bg-blue-400  "
            >Signup</a
          >
        </div>
      </div>
    </div>
    <div class="pt-32">
      <main class="flex space-x-4 ">
        <div class="flex flex-col ml-16 p-4 text-xs bg-gray-100 rounded">
          <div>
            <button
              class="bg-blue-700 py-1 px-5 mb-8 rounded-sm text-white text-sm flex items-center"
              @click="showModal()"
            >
              <span>Create A Post</span>
            </button>
          </div>
          <nuxt-link
            class="m-1 p-1 flex items-center w-64 space-x-2 text-gray-600 rounded-sm"
            to="/Account"
            ><svg
              class="fill-current w-6 h-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 16 16"
            >
              <path
                d="M4.56519,1.42908c-1.3717,-0.865417 -2.9422,-1.34027 -4.56519,-1.42908c0.375244,0.175659 0.746643,0.361145 1.09888,0.583374c0.848633,0.534668 1.37598,1.50293 1.37598,2.52637v2.85352h3v-2.85352c0,-0.682617 -0.348633,-1.32666 -0.909668,-1.68066Z"
                transform="translate(10.525 9.037)"
              />
              <path
                d="M11.0903,1.91797c-3.04004,-1.91797 -7.14111,-1.91797 -10.1802,0c-0.561523,0.353516 -0.910156,0.997559 -0.910156,1.68066v2.85352h12v-2.85352c0,-0.683105 -0.348633,-1.32715 -0.909668,-1.68066Z"
                transform="translate(0 8.548)"
              />
              <path
                d="M0,6.83435c0.323242,0.0978393 0.65686,0.165649 1.0058,0.165649c1.92969,0 3.5,-1.57031 3.5,-3.5c0,-1.92969 -1.57031,-3.5 -3.5,-3.5c-0.348938,0 -0.682556,0.0678101 -1.0058,0.165649c0.917175,0.824341 1.5058,2.00684 1.5058,3.33435c0,1.32751 -0.588623,2.51001 -1.5058,3.33435Z"
                transform="translate(8.994 1)"
              />
              <path
                d="M6.31658,1.36684c1.36684,1.36684 1.36684,3.58291 0,4.94975c-1.36684,1.36684 -3.58291,1.36684 -4.94975,8.88178e-16c-1.36684,-1.36684 -1.36684,-3.58291 -8.88178e-16,-4.94975c1.36684,-1.36684 3.58291,-1.36684 4.94975,-8.88178e-16"
                transform="translate(2.158 .658)"
              />
            </svg>
            <span class="">My Account </span>
          </nuxt-link>
          <nuxt-link
            class="m-1 p-1 flex items-center w-64 space-x-2 text-gray-600 rounded-sm"
            to="/Messages"
            ><svg
              class="fill-current w-6 h-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 16 16"
            >
              <path
                d="M4.56519,1.42908c-1.3717,-0.865417 -2.9422,-1.34027 -4.56519,-1.42908c0.375244,0.175659 0.746643,0.361145 1.09888,0.583374c0.848633,0.534668 1.37598,1.50293 1.37598,2.52637v2.85352h3v-2.85352c0,-0.682617 -0.348633,-1.32666 -0.909668,-1.68066Z"
                transform="translate(10.525 9.037)"
              />
              <path
                d="M11.0903,1.91797c-3.04004,-1.91797 -7.14111,-1.91797 -10.1802,0c-0.561523,0.353516 -0.910156,0.997559 -0.910156,1.68066v2.85352h12v-2.85352c0,-0.683105 -0.348633,-1.32715 -0.909668,-1.68066Z"
                transform="translate(0 8.548)"
              />
              <path
                d="M0,6.83435c0.323242,0.0978393 0.65686,0.165649 1.0058,0.165649c1.92969,0 3.5,-1.57031 3.5,-3.5c0,-1.92969 -1.57031,-3.5 -3.5,-3.5c-0.348938,0 -0.682556,0.0678101 -1.0058,0.165649c0.917175,0.824341 1.5058,2.00684 1.5058,3.33435c0,1.32751 -0.588623,2.51001 -1.5058,3.33435Z"
                transform="translate(8.994 1)"
              />
              <path
                d="M6.31658,1.36684c1.36684,1.36684 1.36684,3.58291 0,4.94975c-1.36684,1.36684 -3.58291,1.36684 -4.94975,8.88178e-16c-1.36684,-1.36684 -1.36684,-3.58291 -8.88178e-16,-4.94975c1.36684,-1.36684 3.58291,-1.36684 4.94975,-8.88178e-16"
                transform="translate(2.158 .658)"
              />
            </svg>
            <span class=""> My Messages</span>
          </nuxt-link>
        </div>
        <div class="max-w-full flex-1">
          <nuxt />
        </div>
      </main>
    </div>
  </main>
</template>

<script>
import { mapGetters } from "vuex";
export default {
  computed: {
    ...mapGetters(["isAuthenticated", "loggedInUser", "getUser"])
  },
  data() {
    return {
      dropdownOpen: false,
      open: false,
      drop: false,
      mode: "",
      isVisible: false,
      groups: [],
      url: "",
      show_modal: false
    };
  },
  methods: {
    showModal() {
      if (this.show_modal) {
        //stop screen scrolling
        this.show_modal = false;
      } else {
        this.show_modal = true;
      }
    }
  }
};
</script>

<style scoped>
.nuxt-link-exact-active {
  border-left: rgb(7, 88, 239) 6px solid;
  background-color: rgb(255, 255, 255);
  color: rgb(32, 105, 230);
}
</style>

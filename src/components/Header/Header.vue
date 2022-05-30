<template>
  <div>
    <header class="text-gray-600 body-font">
      <div
        class="
          container
          mx-auto
          flex flex-wrap
          p-5
          flex-col
          md:flex-row
          items-center
        "
      >
        <a
          class="
            flex
            title-font
            font-medium
            items-center
            text-gray-900
            mb-4
            md:mb-0
          "
        >
          <img
            alt="Geptourist logo"
            style="width: 15rem"
            src="https://geotourist.com/img/logo.2d5bfdcb.png"
          />
        </a>
        <nav
          style="margin-right: 11rem"
          class="
            md:ml-auto
            md:mr-auto
            ml-24
            flex flex-wrap
            items-center
            text-base
            justify-center
          "
        >
          <a class="mr-5 hover:text-gray-900 cursor-pointer">Discover</a>
          <a class="mr-5 hover:text-gray-900 cursor-pointer">Create</a>
          <a class="mr-5 hover:text-gray-900">
            <button
              class="
                inline-flex
                items-center
                bg-gray-400
                border-0
                py-1
                px-3
                focus:outline-none
                hover:bg-gray-300
                rounded
                text-white text-base
                mt-4
                md:mt-0
              "
            >
              Download
            </button>
          </a>
        </nav>
        <button
          class="
            inline-flex
            items-center
            border-0
            py-1
            px-3
            focus:outline-none
            rounded
            text-base
            mt-4
            md:mt-0
          "
        >
          <svg
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="w-8 h-6 ml-1"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 384 512"
          >
            <path
              d="M336 0h-288C21.49 0 0 21.49 0 48v431.9c0 24.7 26.79 40.08 48.12 27.64L192 423.6l143.9 83.93C357.2 519.1 384 504.6 384 479.9V48C384 21.49 362.5 0 336 0zM336 452L192 368l-144 84V54C48 50.63 50.63 48 53.1 48h276C333.4 48 336 50.63 336 54V452z"
            />
          </svg>
        </button>

        <button
          class="
            inline-flex
            items-center
            border-0
            py-1
            px-3
            focus:outline-none
            rounded
            text-base
            mt-4
            md:mt-0
          "
        >
          <svg
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            class="w-8 h-6 ml-1"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 448 512"
          >
            <path
              d="M256 32V49.88C328.5 61.39 384 124.2 384 200V233.4C384 278.8 399.5 322.9 427.8 358.4L442.7 377C448.5 384.2 449.6 394.1 445.6 402.4C441.6 410.7 433.2 416 424 416H24C14.77 416 6.365 410.7 2.369 402.4C-1.628 394.1-.504 384.2 5.26 377L20.17 358.4C48.54 322.9 64 278.8 64 233.4V200C64 124.2 119.5 61.39 192 49.88V32C192 14.33 206.3 0 224 0C241.7 0 256 14.33 256 32V32zM216 96C158.6 96 112 142.6 112 200V233.4C112 281.3 98.12 328 72.31 368H375.7C349.9 328 336 281.3 336 233.4V200C336 142.6 289.4 96 232 96H216zM288 448C288 464.1 281.3 481.3 269.3 493.3C257.3 505.3 240.1 512 224 512C207 512 190.7 505.3 178.7 493.3C166.7 481.3 160 464.1 160 448H288z"
            />
          </svg>
        </button>

        <button
          class="
            inline-flex
            items-center
            border-0
            py-1
            px-3
            focus:outline-none
            rounded
            text-base
            mt-4
            md:mt-0
          "
        >
          <Profile />
        </button>
      </div>
    </header>
    <hr class="mx-auto" />
  </div>
</template>

<script>
import Profile from '../Profile/Profile.vue'

export default {
  name: 'Header',
  components: {
    Profile
  }
}
</script>

<style scoped>
hr {
  border: dotted 1px #dfdcdc;
  max-width: 1500px;
}
</style>

<template>
  <!-- Project Layout -->

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
    <div class="dropdown">
      <button class="btn dropdown-toggle" type="button" data-toggle="dropdown">
        <v-avatar></v-avatar>
      </button>
    </div>

    <div class="dropdown">
      <button class="dropbtn">
        <img
          style="width: 4rem; border-radius: 100%"
          src="https://cdn.vuetifyjs.com/images/john.jpg"
          alt="John"
        />
      </button>
      <div class="dropdown-content">
        <a href="#" class="">
          <div class="flex justify-between">
            <div class="icon mt-4">
              <img
                style="width: 2.5rem; border-radius: 100%"
                src="https://cdn.vuetifyjs.com/images/john.jpg"
                alt="John"
              />
            </div>
            <div class="text ml-4">
              <div class="name mt-4 mr-6">Lawrence Power</div>
              <br />
              <p>My Page</p>
            </div>
            <div class="icon mt-4">
              <img
                style="width: 2.5rem; border-radius: 100%"
                src="data:image/png;base64,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"
                alt="John"
              />
            </div>
          </div>
        </a>
        <hr />
        <a href="#" class="">
          <div class="flex">
            <div class="icon">
              <svg
                stroke="blue"
                fill="skyBlue"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                class="w-8 h-6 ml-1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
              >
                <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                <path
                  d="M256 112c-48.6 0-88 39.4-88 88C168 248.6 207.4 288 256 288s88-39.4 88-88C344 151.4 304.6 112 256 112zM256 240c-22.06 0-40-17.95-40-40C216 177.9 233.9 160 256 160s40 17.94 40 40C296 222.1 278.1 240 256 240zM256 0C114.6 0 0 114.6 0 256s114.6 256 256 256s256-114.6 256-256S397.4 0 256 0zM256 464c-46.73 0-89.76-15.68-124.5-41.79C148.8 389 182.4 368 220.2 368h71.69c37.75 0 71.31 21.01 88.68 54.21C345.8 448.3 302.7 464 256 464zM416.2 388.5C389.2 346.3 343.2 320 291.8 320H220.2c-51.36 0-97.35 26.25-124.4 68.48C65.96 352.5 48 306.3 48 256c0-114.7 93.31-208 208-208s208 93.31 208 208C464 306.3 446 352.5 416.2 388.5z"
                />
              </svg>
            </div>
            <div class="text ml-4">Edit Profile</div>
          </div>
        </a>
        <hr style="color: blue" />
        <a href="#" class="">
          <div class="flex">
            <div class="icon">
              <svg
                stroke="blue"
                fill="skyBlue"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                class="w-8 h-6 ml-1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
              >
                <path
                  d="M495.9 166.6C499.2 175.2 496.4 184.9 489.6 191.2L446.3 230.6C447.4 238.9 448 247.4 448 256C448 264.6 447.4 273.1 446.3 281.4L489.6 320.8C496.4 327.1 499.2 336.8 495.9 345.4C491.5 357.3 486.2 368.8 480.2 379.7L475.5 387.8C468.9 398.8 461.5 409.2 453.4 419.1C447.4 426.2 437.7 428.7 428.9 425.9L373.2 408.1C359.8 418.4 344.1 427 329.2 433.6L316.7 490.7C314.7 499.7 307.7 506.1 298.5 508.5C284.7 510.8 270.5 512 255.1 512C241.5 512 227.3 510.8 213.5 508.5C204.3 506.1 197.3 499.7 195.3 490.7L182.8 433.6C167 427 152.2 418.4 138.8 408.1L83.14 425.9C74.3 428.7 64.55 426.2 58.63 419.1C50.52 409.2 43.12 398.8 36.52 387.8L31.84 379.7C25.77 368.8 20.49 357.3 16.06 345.4C12.82 336.8 15.55 327.1 22.41 320.8L65.67 281.4C64.57 273.1 64 264.6 64 256C64 247.4 64.57 238.9 65.67 230.6L22.41 191.2C15.55 184.9 12.82 175.3 16.06 166.6C20.49 154.7 25.78 143.2 31.84 132.3L36.51 124.2C43.12 113.2 50.52 102.8 58.63 92.95C64.55 85.8 74.3 83.32 83.14 86.14L138.8 103.9C152.2 93.56 167 84.96 182.8 78.43L195.3 21.33C197.3 12.25 204.3 5.04 213.5 3.51C227.3 1.201 241.5 0 256 0C270.5 0 284.7 1.201 298.5 3.51C307.7 5.04 314.7 12.25 316.7 21.33L329.2 78.43C344.1 84.96 359.8 93.56 373.2 103.9L428.9 86.14C437.7 83.32 447.4 85.8 453.4 92.95C461.5 102.8 468.9 113.2 475.5 124.2L480.2 132.3C486.2 143.2 491.5 154.7 495.9 166.6V166.6zM256 336C300.2 336 336 300.2 336 255.1C336 211.8 300.2 175.1 256 175.1C211.8 175.1 176 211.8 176 255.1C176 300.2 211.8 336 256 336z"
                />
              </svg>
            </div>
            <div class="text ml-4">Settings</div>
          </div>
        </a>
        <hr />
        <a href="#" class="">
          <div class="flex">
            <div class="icon">
              <svg
                stroke="blue"
                fill="skyBlue"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                class="w-8 h-6 ml-1"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
              >
                <path
                  d="M400 54.1c63 45 104 118.6 104 201.9 0 136.8-110.8 247.7-247.5 248C120 504.3 8.2 393 8 256.4 7.9 173.1 48.9 99.3 111.8 54.2c11.7-8.3 28-4.8 35 7.7L162.6 90c5.9 10.5 3.1 23.8-6.6 31-41.5 30.8-68 79.6-68 134.9-.1 92.3 74.5 168.1 168 168.1 91.6 0 168.6-74.2 168-169.1-.3-51.8-24.7-101.8-68.1-134-9.7-7.2-12.4-20.5-6.5-30.9l15.8-28.1c7-12.4 23.2-16.1 34.8-7.8zM296 264V24c0-13.3-10.7-24-24-24h-32c-13.3 0-24 10.7-24 24v240c0 13.3 10.7 24 24 24h32c13.3 0 24-10.7 24-24z"
                />
              </svg>
            </div>
            <div class="text ml-4">Logout</div>
          </div>
        </a>
        <hr />
        <a href="#" class="">
          <div class="flex justify-between">
            <div class="text ml-4">English</div>
            <div class="icon text-blue-300">></div>
          </div>
        </a>
      </div>
    </div>
  </button>

  <!-- Template layout -->

  <div class="background"></div>
</template>

<script>
export default {
  name: 'Profile'
}
</script>

<style scoped>
.dropbtn {
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #ffffff;
  min-width: 280px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
  border: 8px !important;
}

.dropdown-content a {
  color: black;
  padding: 20px 20px;
  text-decoration: none;
  display: block;
  text-align: left;
}

.dropdown-content a:hover {
  background-color: #ddd;
}

.dropdown:hover .dropdown-content {
  display: block;
}
</style>

<template>
  <section class="about_section py-24">
    <div class="container mx-auto">
      <div class="flex flex-col-reverse lg:flex-row items-center">
        <div class="w-full lg:w-1/2">
          <div class="img_container">
            <div class="img-box">
              <img src="images/about-img.jpg" alt="About Us Image" class="w-full" />
            </div>
          </div>
        </div>
        <div class="w-full lg:w-1/2 bg-white shadow-md relative -ml-11 p-6 lg:p-8">
          <div class="heading_container mb-4">
            <h2 class="text-3xl font-bold">
              Who Are We?
            </h2>
          </div>
          <p class="mt-2 text-gray-600">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
            enim ad minim veniam, quis nostrud exercitation ullamco laboris
            nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor
            in reprehenderit in voluptate velit.
          </p>
          <div class="btn-box mt-4">
            <a href="" class="inline-block bg-yellow-400 text-white py-2 px-8 uppercase transition duration-300 border border-transparent hover:bg-transparent hover:text-yellow-400 hover:border-yellow-400">
              Read More
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutSection",
};
</script>

<style scoped>

.about_section {
  @apply relative;
}

.img_container .img-box {
  @apply w-full;
}

.detail-box {
  @apply bg-white shadow-md relative p-6 lg:p-8 -ml-11;
}

.heading_container {
  @apply mb-4;
}

.btn-box a {
  @apply inline-block bg-yellow-400 text-white py-2 px-8 uppercase transition duration-300 border border-transparent hover:bg-transparent hover:text-yellow-400 hover:border-yellow-400;
}
</style>

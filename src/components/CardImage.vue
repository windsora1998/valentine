<template>
  <div class="rounded overflow-hidden shadow-lg flex flex-col border-[1px] border-[#c9184a]">
    <a href="#!"></a> 
    <div class="relative"><a href="#">
        <img class="w-full h-[600px]" v-bind:src="url" alt="Sunset in the mountains">
        <div
          class="hover:bg-transparent transition duration-300 absolute bottom-0 top-0 right-0 left-0 ">
        </div>
      </a>
      <a href="#!">
        <div
          class="text-xs absolute top-0 right-0 bg-[#c9184a] px-4 py-2 text-white mt-3 mr-3 transition duration-500 ease-in-out">
          {{date}}
        </div>
      </a>
    </div>
    <div class="bg-[#dd6c8c] text-white px-6 py-4 mb-auto">
      <a href="#!"
        class="font-medium text-lg  inline-block transition duration-500 ease-in-out mb-2">
        {{ content }}</a>
    </div>
  </div>
</template>

<script>

export default {
  name: 'CardImage',
  props: {
    url: String,
    date: String,
    content: String
  }
}
</script>

<style>
img {
  object-fit: contain;
}

div {
  font-family:  Helvetica, Arial, sans-serif;

}
</style>

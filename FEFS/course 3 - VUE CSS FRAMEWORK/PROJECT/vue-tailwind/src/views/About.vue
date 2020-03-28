<template>
  <div class="about min-h-screen bg-cover" :style="{backgroundImage: `url('${image}')`}">
    <div class="pt-32 pl-40 mb-2">
      <img src="@/assets/hacktiv8.png" alt="">
    </div>

    <div class="pl-40 mb-4">
      <button class="px-6 py-2 bg-white text-black font-bold uppercase rounded flex items-center hover:bg-gray-300">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path class="heroicon-ui" d="M17 11a1 1 0 0 1 0 2h-4v4a1 1 0 0 1-2 0v-4H7a1 1 0 0 1 0-2h4V7a1 1 0 0 1 2 0v4h4z"/></svg>
        <span class="pl-1">Join</span>
      </button>
    </div>

    <div class="pl-40 text-gray-500 mb-8">
      &copy; 2020 &middot; FEBS &middot; FEFS &middot; BESN &middot; DASN &middot; MLSN
    </div>

    <div class="w-96 xl:w-1/2 pl-40 leading-loose">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Natus fugit tenetur velit quasi soluta sunt suscipit, eveniet dolorum. Tenetur architecto voluptatum quis, vitae autem, vero tempora libero impedit culpa debitis, quisquam nam nemo quidem modi sunt illo consequuntur maiores magni.
    </div>
  </div>
</template>

<script>

export default {
  name: 'About',
  data(){
    return {
      image: require('@/assets/background-copy.jpg')
    }
  }
}

</script>
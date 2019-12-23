<template>
  <div>
     <LightGallery
      background="rgb(255, 255, 255, .9)"
      :images="images"
      :index="index"
      :disable-scroll="true"
      @close="index = null"
    />
    <ul>
      <li
        v-for="(thumb, thumbIndex) in [
          '/imgs/thumbs/01-Mazzata 2.0.gif',
          '/imgs/thumbs/02-Devastation.gif',
          '/imgs/thumbs/03-Mazzata.gif',
          '/imgs/thumbs/04-Tempesta.gif',
          '/imgs/thumbs/05-Blade.gif',
          '/imgs/thumbs/06-Final Blade.gif',
          '/imgs/thumbs/07-Killer Evolution.gif',
          '/imgs/thumbs/08-Evolutiuon.gif',
          '/imgs/thumbs/09-Evolution H2O.gif',
          '/imgs/thumbs/10-Final Evolution.gif',
          '/imgs/thumbs/11-Hyper Evo.gif',
          '/imgs/thumbs/12-Coyote Bravo.gif',
          '/imgs/thumbs/13-Frusta.gif',
          '/imgs/thumbs/14-Techno Defence.gif'
        ]"
        :key="thumbIndex"
        @click="index = thumbIndex"
      >
        <img :src="thumb">
      </li>
    </ul>
  </div>
</template>

<script>
  import { LightGallery } from 'vue-light-gallery';

  export default {
    name: 'JaegerGallery',
    components: {
      LightGallery,
    },
    data() {
      return {
        images: [
          {title: 'Mazzata 2', url: '/imgs/01-Mazzata 2.0.gif'},
          {title: 'Devastation', url: '/imgs/02-Devastation.gif'},
          {title: 'Mazzata', url: '/imgs/03-Mazzata.gif'},
          {title: 'Tempesta', url: '/imgs/04-Tempesta.gif'},
          {title: 'Blade', url: '/imgs/05-Blade.gif'},
          {title: 'Final Blade', url: '/imgs/06-Final Blade.gif'},
          {title: 'Killer Evolution', url: '/imgs/07-Killer Evolution.gif'},
          {title: 'Evolutiuon', url: '/imgs/08-Evolutiuon.gif'},
          {title: 'Evolution H2O', url: '/imgs/09-Evolution H2O.gif'},
          {title: 'Final Evolution', url: '/imgs/10-Final Evolution.gif'},
          {title: 'Hyper Evo', url: '/imgs/11-Hyper Evo.gif'},
          {title: 'Coyote Bravo', url: '/imgs/12-Coyote Bravo.gif'},
          {title: 'Frusta', url: '/imgs/13-Frusta.gif'},
          {title: 'Techno Defence', url: '/imgs/14-Techno Defence.gif'}
        ],
        index: null,
      };
    },
  };
</script>

<style scoped>
  ul {
    list-style: none;
  }
  li {
    display: inline-block;
    margin: 10px;
    cursor: pointer;
    overflow: hidden;
    border-radius: 3px;
    box-shadow: 0px 1px 4px rgba(0, 0, 0, 0.5);
  }
</style>

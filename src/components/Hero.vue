<template>
    
    <div class="heroBlock">
        <v-carousel hide-delimiters cycle :show-arrows="false">
            <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade-transition"
            transition="fade-transition"
            >
                <v-row class="fill-height title hidden-xs-only" align="center" justify="center">
                    <div>
                         {{ item.title }}
                    </div>
                </v-row>
            </v-carousel-item>
        </v-carousel>
    </div>
    
</template>

<script>
  export default {
    name: 'Hero',

    data: () => ({
      items: [
          {
            src: require("../assets/images/carrousel-1.jpg"),
            title:"We are creative "
          },
          {
            src: require("../assets/images/carrousel-2.jpg"),
            title:"We are hard worker "
          },
          {
            src: require("../assets/images/carrousel-3.jpg"),
            title:"We are professional "
          },
        ],
    }),
  }
</script>

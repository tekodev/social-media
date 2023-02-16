<template>
  <div class="app-container">
    <v-row>
      <v-col
        cols="12"
        md="3"
      >
        <ProfileCard />
      </v-col>
      <v-col
        cols="12"
        md="6"
      >
        <Content />
      </v-col>
      <v-col
        cols="12"
        md="3"
      >
        <Links />
      </v-col>
    </v-row>
  </div>
  
</template>

<script>
  import ProfileCard from '@/components/ProfileCard.vue';
  import Content from '@/components/Content.vue';
  import Links from '@/components/Links.vue';


  export default {
    name: 'Home',

    components: {
      ProfileCard,
      Content,
      Links
    },
  }
</script>

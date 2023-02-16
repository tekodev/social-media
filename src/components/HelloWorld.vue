<template>
  <div class="app-container">
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to Vuetify
        </h1>

        <p class="subheading font-weight-regular">
          For help and collaboration with other Vuetify developers,
          <br>please join our online
          <a
            href="https://community.vuetifyjs.com"
            target="_blank"
          >Discord Community</a>
        </p>
      </v-col>
      <br>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident aspernatur dolorum aut doloribus vitae, consequuntur magni veniam enim ea nemo temporibus quaerat, accusamus recusandae. Eos placeat veritatis beatae rerum alias, iusto sit aperiam fugiat suscipit, nam temporibus assumenda quo? Impedit vero architecto omnis odio esse placeat voluptas, delectus molestiae provident eligendi reiciendis temporibus excepturi error itaque quasi mollitia ipsam ad consequatur rerum! Esse quis obcaecati quibusdam voluptas modi beatae iusto similique harum neque mollitia odit consequuntur asperiores dolor, repellat dicta dignissimos! Vero dolorem, sit sequi explicabo rerum accusantium voluptatibus inventore ipsum alias, quod ullam possimus modi beatae nihil asperiores? Eum deserunt praesentium quidem, facilis hic magnam quisquam accusamus unde ullam dolor, vel alias incidunt delectus omnis veniam ipsam repellat, sapiente doloribus recusandae doloremque soluta reiciendis. At minus dicta facere velit libero deleniti, odit neque recusandae enim eos iste ut voluptate et cumque odio hic. Provident fugiat velit pariatur est odio dolore consequatur nulla laudantium vitae, perferendis incidunt enim dicta rem vel quia quos magni exercitationem sed impedit! Ducimus, provident facilis! Fuga vero nam, totam ab voluptatem ut illo nulla quidem. Veniam eum optio assumenda dolorem aliquam. Nemo debitis veniam reprehenderit recusandae, a inventore, sequi accusantium assumenda vel repellat error expedita ad, laboriosam eius voluptatem earum. Exercitationem vel, earum ad maxime sequi mollitia cupiditate itaque fuga perferendis officia incidunt, sunt possimus inventore id, ratione fugiat consequatur numquam illo eligendi corrupti alias! Fugiat omnis blanditiis nulla provident ipsam ratione, tempore repudiandae laborum corporis veritatis accusamus temporibus officiis nisi perspiciatis alias atque ex beatae quisquam dicta magnam voluptates natus et non! Quis ex quasi repellat quia ab adipisci sed natus minus atque cum omnis tenetur harum officiis, asperiores eligendi ratione sapiente! Reprehenderit voluptatibus suscipit esse quo! Dicta, non, alias dolores eligendi quaerat eum commodi qui illo officiis, consequuntur unde minima atque blanditiis cumque.

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          What's next?
        </h2>

        <v-row justify="center">
          <a
            v-for="(next, i) in whatsNext"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          Important Links
        </h2>

        <v-row justify="center">
          <a
            v-for="(link, i) in importantLinks"
            :key="i"
            :href="link.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ link.text }}
          </a>
        </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          Ecosystem
        </h2>

        <v-row justify="center">
          <a
            v-for="(eco, i) in ecosystem"
            :key="i"
            :href="eco.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ eco.text }}
          </a>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      ecosystem: [
        {
          text: 'vuetify-loader',
          href: 'https://github.com/vuetifyjs/vuetify-loader',
        },
        {
          text: 'github',
          href: 'https://github.com/vuetifyjs/vuetify',
        },
        {
          text: 'awesome-vuetify',
          href: 'https://github.com/vuetifyjs/awesome-vuetify',
        },
      ],
      importantLinks: [
        {
          text: 'Documentation',
          href: 'https://vuetifyjs.com',
        },
        {
          text: 'Chat',
          href: 'https://community.vuetifyjs.com',
        },
        {
          text: 'Made with Vuetify',
          href: 'https://madewithvuejs.com/vuetify',
        },
        {
          text: 'Twitter',
          href: 'https://twitter.com/vuetifyjs',
        },
        {
          text: 'Articles',
          href: 'https://medium.com/vuetify',
        },
      ],
      whatsNext: [
        {
          text: 'Explore components',
          href: 'https://vuetifyjs.com/components/api-explorer',
        },
        {
          text: 'Select a layout',
          href: 'https://vuetifyjs.com/getting-started/pre-made-layouts',
        },
        {
          text: 'Frequently Asked Questions',
          href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
        },
      ],
    }),
  }
</script>

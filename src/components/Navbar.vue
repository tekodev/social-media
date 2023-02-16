<template>
    <div class="mb-7">
        <v-app-bar app color="white">
            <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="d-flex d-lg-none justify-start items-center"></v-app-bar-nav-icon>
            <div class="app-container d-flex align-center">

                <span class="hidden-md-and-up">
                    <v-toolbar-side-icon @click="sidebar = !sidebar">
                    </v-toolbar-side-icon>
                </span>
                <v-toolbar-title>
                    <router-link to="/" tag="span" style="cursor: pointer">
                        <img height="36" src="https://packted.com/wp-content/uploads/2022/04/cropped-Packted-logo-Website-1.png" alt="">
                    </router-link>
                </v-toolbar-title>
                <v-toolbar-items class="hidden-md-and-down" icons-and-text>
                    <router-link class="nav-link px-5" v-for="item in items" :key="item.title" :to="item.path" color="white">
                        {{ item.title }}    
                        <v-icon color="primary" large>{{ item.icon }}</v-icon>
                    </router-link>
                </v-toolbar-items>
                <v-text-field class="px-2 hidden-md-and-down" hide-details outlined label="Search" prepend-inner-icon="mdi-magnify"></v-text-field>
                <v-btn
                    color="primary"
                    class="navbar-button mx-2 px-10 hidden-md-and-down"
                >
                Keşfet
                </v-btn>
                <router-link to="/" tag="span" class="nav-link px-5 hidden-md-and-down">
                    <span class="ma-auto">{{ userName }}</span>
                    <img height="35" class="sendbox-profile-photo" :src="userPhoto" />
                </router-link>

                <v-divider class="mx-4 hidden-md-and-down" inset vertical></v-divider>

                <template>
                    <div class="text-center hidden-md-and-down">
                        <v-menu offset-y >
                        <template v-slot:activator="{ on, attrs }">
                            <div
                            color="white"
                            light
                            v-bind="attrs"
                            v-on="on"
                            class="nav-link"
                            >
                            <span>&nbsp; Operasyonlar<v-icon color="primary">mdi-menu-down</v-icon></span>
                            <v-icon color="primary" large>mdi-file-cog</v-icon>
                        </div>
                        </template>
                        <v-list>
                            <v-list-item
                                v-for="(item, index) in operations"
                                :key="index"
                                >
                                <v-list-item-title>{{ item.title }}</v-list-item-title>
                            </v-list-item>
                        </v-list>
                        </v-menu>
                    </div>
                </template>

                <template>
                    <div class="text-center hidden-md-and-down">
                        <v-menu offset-y >
                            <template v-slot:activator="{ on, attrs }">
                                <div
                                color="white"
                                light
                                v-bind="attrs"
                                v-on="on"
                                class="nav-link"
                                >
                                <span>&nbsp; Servisler<v-icon color="primary">mdi-menu-down</v-icon></span>
                                <v-icon color="primary" large>mdi-application-cog-outline</v-icon>
                            </div>
                            </template>
                            <v-list>
                                <v-list-item
                                    v-for="(item, index) in services"
                                    :key="index"
                                    >
                                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                                </v-list-item>
                            </v-list>
                        </v-menu>
                    </div>
                </template>
            </div>
        </v-app-bar>
        <v-navigation-drawer app v-model="drawer" :clipped="$vuetify.breakpoint.lgAndUp">
            <v-list>
                <v-list-item v-for="(item, index) in items" :key="index" @click="drawer = false">
                    <v-list-item-action>
                        <v-icon>{{ item.icon }}</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </div>
  </template>
  
  <script>
import router from '@/router';

  export default {
    name: "Navbar",
    data() {
        return {
            drawer: false,
            appTitle: "Soical Media",
            userName: "Profil",
            userPhoto : "https://cdn.vuetifyjs.com/images/profiles/marcus.jpg",
            items: [
                { title: "Bildirimler", icon: "mdi-bell", path: "/1" },
                { title: "Mesajlaşma", icon: "mdi-message-processing", path: "/2" },
                { title: "Bağlantılarım", icon: "mdi-account-multiple", path: "/3" },
                { title: "İş Ortaklarım", icon: "mdi-handshake", path: "/4" },
            ],
            operations: [
                { title: "Operasyon 1", path: "/1" },
                { title: "Operasyon 2", path: "/2" },
                { title: "Operasyon 3", path: "/3" },
                { title: "Operasyon 4", path: "/4" },
            ],
            services : [
                { title: "Servis 1", path: "/1" },
                { title: "Servis 2", path: "/2" },
                { title: "Servis 3", path: "/3" },
                { title: "Servis 4", path: "/4" },
            ]

        };
    },
    components: { router }
};
  </script>

<style scoped>

.nav-link {
    display: flex;
    flex-direction: column-reverse;
    text-decoration:none;
    color: black !important;
    white-space: nowrap;
    cursor: pointer;
}

.navbar-button {
    height: 56px !important;
    box-shadow: none;
}


</style>
  
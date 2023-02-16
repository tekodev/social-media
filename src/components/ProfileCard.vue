<template>
    <v-card class="mx-auto rounded">
        <v-img height="100" src="https://cdn.vuetifyjs.com/images/cards/server-room.jpg"></v-img>
        <v-col class="d-flex justify-center">
            <v-avatar size="100" class="avatar-box">
                <v-img src="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"></v-img>
            </v-avatar>
        </v-col>
        <v-list-item color="rgba(0, 0, 0, .4)">
            <v-list-item-content class="mt-5">
                <v-list-item-title class="title text-center font-weight-bold">{{ profileName }}</v-list-item-title>
                <v-list-item-subtitle class="text-center font-weight-bold mt-3"> {{ profileDes }}</v-list-item-subtitle>
            </v-list-item-content>
        </v-list-item>
        <v-list subheader>
            <v-list-item>
                <v-list-item-avatar>
                    <v-icon color="primary"> mdi-account-multiple </v-icon>
                </v-list-item-avatar>
                <v-list-item-content>
                    <v-list-item-title class="font-weight-bold primary--text">Bağlantılarım</v-list-item-title>
                </v-list-item-content>
                <v-list-item-action class="font-weight-bold">{{ numberOfConnections }}</v-list-item-action>
            </v-list-item>

            <v-list-item>
                <v-list-item-avatar>
                    <v-icon color="primary"> mdi-handshake </v-icon>
                </v-list-item-avatar>
                <v-list-item-content>
                    <v-list-item-title class="font-weight-bold primary--text">İş Ortaklarım</v-list-item-title>
                </v-list-item-content>
                <v-list-item-action class="font-weight-bold">{{ numberOfPartnership }}</v-list-item-action>
            </v-list-item>

            <v-list-item>
                <v-list-item-avatar>
                    <v-icon color="primary"> mdi-eye </v-icon>
                </v-list-item-avatar>
                <v-list-item-content>
                    <v-list-item-title class="font-weight-bold primary--text">Görüntülenme</v-list-item-title>
                </v-list-item-content>
                <v-list-item-action class="font-weight-bold">{{ numberOfViews }}</v-list-item-action>
            </v-list-item>

            <v-list-item>
                <v-list-item-avatar>
                    <v-icon disabled> mdi-content-save </v-icon>
                </v-list-item-avatar>
                <v-list-item-content>
                    <v-list-item-title class="font-weight-bold profile-view-your-saved">Kaydedilenleri Görüntüle</v-list-item-title>
                </v-list-item-content>
            </v-list-item>

            <v-list-item>
                <v-list-item-content>
                    <v-list-item-title class="font-weight-bold success--text text-center">Premium'u Ücretsiz Dene</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </v-list>
    </v-card>
</template>

<script>
  export default {
    name: 'ProfileCard',
    data() {
        return {
            profileName: "Bessie Cooper",
            profileDes : "Business Development",
            numberOfConnections : "126",
            numberOfPartnership : "321",
            numberOfViews : "123.321"

        };
    },
  }
  
</script>

<style>

.avatar-box {
    position:absolute; 
    top: 47px;
    border: solid 5px white;
}

.primary--text {
    color: #1976d2;
}

.profile-view-your-saved {
    color: #9e9b9b !important;
}

</style>
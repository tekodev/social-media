<template>
    <div>
        <v-card elevation="0" class="px-5 py-4">
            <v-text-field class="photo-box" outlined hide-details type="text" :placeholder="profileName + ', bugün ne düşünüyorsun.'">
                <template v-slot:prepend d-flex align-center>
                    <v-tooltip>
                        <template v-slot:activator="{ on }">
                            <img height="56" class="sendbox-profile-photo" :src="userPhoto" />
                        </template>
                    </v-tooltip>
                </template>
                <template v-slot:append>
                    <v-fade-transition leave-absolute>
                        <v-row style="white-space: nowrap;" justify="space-around">
                            <v-btn elevation="0" color="white" class="me-3 mt-1 text-transform-none primary--text"> Gönderi <v-icon right large> mdi-menu-left </v-icon>
                            </v-btn>
                        </v-row>
                    </v-fade-transition>
                </template>
            </v-text-field>
        </v-card>
        <v-row class="pa-3 align-center justify-space-between">
            <template>
                <div class="text-center">
                    <v-menu offset-y>
                        <template v-slot:activator="{ on, attrs }">
                            <div color="white" light v-bind="attrs" v-on="on">
                                <span class="font-weight-bold">
                                    <v-icon color="dark" large>mdi-menu-down</v-icon>Gönderi
                                </span>
                            </div>
                        </template>
                        <v-list>
                            <v-list-item>
                                <v-list-item-title>Yukarıdan Aşağı</v-list-item-title>
                            </v-list-item>
                            <v-list-item>
                                <v-list-item-title>Aşağıdan Yukarı</v-list-item-title>
                            </v-list-item>
                        </v-list>
                    </v-menu>
                </div>
            </template>
            <label for="filter" class="mx-3 info-text-color">Fitrele</label>
            <v-text-field name="filter"></v-text-field>
            <label for="sorting" class="mx-3 info-text-color">Sıralama Ölçümü</label>
            <template name="sorting">
                <div class="text-center">
                    <v-menu offset-y>
                        <template v-slot:activator="{ on, attrs }">
                            <div color="white" light v-bind="attrs" v-on="on">
                                <span class="font-weight-bold">&nbsp;En Önemli <v-icon large color="dark">mdi-menu-down</v-icon>
                                </span>
                            </div>
                        </template>
                        <v-list>
                            <v-list-item>
                                <v-list-item-title>En Popüler</v-list-item-title>
                            </v-list-item>
                            <v-list-item>
                                <v-list-item-title>En Yaygın</v-list-item-title>
                            </v-list-item>
                        </v-list>
                    </v-menu>
                </div>
            </template>
        </v-row>
        <v-card elevation="0" class="px-5 py-4">
            <v-row>
                <v-col cols="12" lg="6">
                    <div class="justify-space-between d-flex">
                        <v-btn variant="flat" disabled class="text-transform-none"> Gönderi </v-btn>
                        <v-btn variant="flat" class="text-transform-none" elevation="0" color="white">
                            <span class="primary--text select-button">
                                <v-icon class="me-2" color="primary">mdi-account-tie</v-icon>Human Resource
                            </span>
                        </v-btn>
                    </div>
                </v-col>
                <v-col cols="12" lg="6">
                    <div class="justify-space-between d-flex">
                        <v-btn variant="flat" class="text-transform-none" elevation="0" color="white">
                            <span class="primary--text select-button">
                                <v-icon class="me-2" color="blue">mdi-city</v-icon>Gragona
                            </span>
                        </v-btn>
                        <v-btn variant="flat" class="text-transform-none" elevation="0" color="white">
                            <span class="success--text select-button">
                                <v-icon class="me-2" color="success">mdi-earth</v-icon>Türkiye/İstanbul
                            </span>
                        </v-btn>
                    </div>
                </v-col>
            </v-row>
            <v-card-actions>
                <v-list-item class="grow">
                    <v-list-item-avatar color="grey darken-3">
                        <v-img class="elevation-6" alt="" src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"></v-img>
                    </v-list-item-avatar>
                    <v-list-item-content>
                        <v-list-item-title>Marvin McKinney</v-list-item-title>
                        <v-list-item-subtitle class="info-text-color font-weight-bold mt-1">10 Saat Önce</v-list-item-subtitle>
                    </v-list-item-content>
                    <v-row align="center" justify="end">
                        <v-btn variant="text" icon="mdi-dots-vertical">
                            <v-icon> mdi-dots-vertical </v-icon>
                        </v-btn>
                    </v-row>
                </v-list-item>
            </v-card-actions>
            <v-card-text class="text-h6 pt-0"> Turns out semicolon-less style is easier and safer in TS because most gotcha edge cases are type invalid as well.Turns out semicolon-less style is easier... <a style="text-decoration:none;" href="#">Devamını oku</a>
            </v-card-text>
            <v-card-text class="info-text-color d-flex">
                <span>
                    <v-icon class="me-2"> mdi-eye </v-icon> 6.786 Görüntülenme
                </span>
                <span class="ml-auto me-3">95 Yorum</span>
                <span>6 Paylaşım</span>
            </v-card-text>
            <v-card-text class="info-text-color d-flex pt-0 align-center">
                <v-btn variant="flat" class="text-transform-none me-2" elevation="0" color="white">
                    <span class="info-text-color">
                        <v-icon class="me-2">mdi-heart</v-icon>Beğen
                    </span>
                </v-btn>
                <v-btn variant="flat" class="text-transform-none me-2" elevation="0" color="white">
                    <span class="info-text-color">
                        <v-icon class="me-2">mdi-message-processing</v-icon>Yorum Yap
                    </span>
                </v-btn>
                <v-btn variant="flat" class="text-transform-none me-2" elevation="0" color="white">
                    <span class="info-text-color">
                        <v-icon class="me-2">mdi-share</v-icon>Paylaş
                    </span>
                </v-btn>
                <span class="ml-auto">Mehmet Hatip ve 244 diğer kişi</span>
            </v-card-text>
        </v-card>
    </div>
</template>

<script>
  export default {
    name: 'Content',
    data() {
        return {
            profileName: "Bessie Cooper",
            userPhoto : "https://cdn.vuetifyjs.com/images/profiles/marcus.jpg",
        };
    },
  }
  
</script>

<style>

.sendbox-profile-photo {
    border-radius: 100%;
}

.text-transform-none{
    text-transform : none;
}

.photo-box .v-input__prepend-outer{
    margin-top:0;
}

.info-text-color {
    color: #9e9b9b !important;
}

.select-button {
    font-size: 0.8rem;
}

</style>
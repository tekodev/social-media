<template>
    <v-card class="mx-auto rounded" tile>
        <v-list-item class="grow">
            <v-list-item-content>
                <v-list-item-title>Önerilen Bağlantılar</v-list-item-title>
            </v-list-item-content>
            <v-row align="center" justify="end">
                <v-btn variant="text" icon="mdi-dots-vertical">
                    <v-icon> mdi-dots-vertical </v-icon>
                </v-btn>
            </v-row>
        </v-list-item>
        <v-list subheader v-for="(item) in connections" :key="item.id">
            <v-list-item class="grow">
                <v-btn class="ma-2 rounded-xl text-transform-none" outlined color="primary" elevation="0"> Bağlantı Kur </v-btn>
                <v-list-item-content class="text-end">
                    <v-list-item-title>{{ item.name }}</v-list-item-title>
                    <v-list-item-subtitle class="info-text-color font-weight-bold mt-1">{{ item.title }}</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-avatar color="grey darken-3">
                    <v-img class="elevation-6" alt="" :src="item.image"></v-img>
                </v-list-item-avatar>
            </v-list-item>
        </v-list>
        <v-list-item>
                <v-list-item-content>
                    <v-list-item-title class="font-weight-bold primary--text text-center">Tüm Önerileri Görüntüle</v-list-item-title>
                </v-list-item-content>
        </v-list-item>
    </v-card>
</template>

<script>
  export default {
    name: 'Links',
    data() {
        return {
            connections: [
                { 
                    id : 1, 
                    name : "Courtney Henry",
                    title : "Marketing Coordinator",
                    image : "https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                },
                { 
                    id : 2, 
                    name : "Brooklyn Simmons",
                    title : "Web Designer",
                    image : "https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                },
                { 
                    id : 3, 
                    name : "Eleanor Pena",
                    title : "Medical Assistant",
                    image : "https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                },
                { 
                    id : 4, 
                    name : "Esther Howard",
                    title : "Dog Trainer",
                    image : "https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                },
                { 
                    id : 5, 
                    name : "Floydi Miler",
                    title : "Nursing Assistant",
                    image : "https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                },
                { 
                    id : 6, 
                    name : "Savana Nguyen",
                    title : "Medical Assistant",
                    image : "https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                },
            ]
        };
    },
  }
  
</script>

<style>

.primary--text {
    color: #1976d2;
}

</style>
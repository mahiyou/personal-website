<template>
    <v-container class="portfolio-container">
        <div class="page-title">Portfolio</div>
        <div class="mb-12">You can see some of my recent projects here:</div>
        <v-row class="border-project">
            <v-col cols="12" md="5"> <v-img src="../assets/pics/jeydomain.jpg" class="mx-auto" max-height="300px" width="300px" @click="overlayDomain = !overlayDomain"></v-img></v-col>
            <v-overlay v-model="overlayDomain" class="align-center justify-center"><v-img src="../assets/pics/jeydomain-com.jpg"  height="600" width="600" @click="overlayDomain = !overlayDomain"></v-img></v-overlay>
            <v-col cols="12" md="7">
                <div>
                    <div class="text-white font-weight-bold">Front-End of Jey Domain site with vuetify</div>
                    Jey Domain is a front-end of a domain ordering site. User can order and buy different kind of domains in this site.<br />
                    Features:<br />
                    - Knowing different kind of domains.<br />
                    - Find suitable domain for specific purposes.<br />
                    - Set personal configuration for ordered domain.<br />
                    <v-btn class="mt-5 mr-3" variant="outlined" href="https://github.com/mahiyou/jey-domain-vuetify" width="170px"><v-icon class="mr-2">mdi-github</v-icon>source code</v-btn>
                    <v-btn class="mt-5" variant="outlined" width="170px" href="http://jeydomain.mahiyou.net"><v-icon class="mr-2" >mdi-view-dashboard-outline</v-icon>live preview</v-btn>
                </div>
            </v-col>
        </v-row>
        <v-row class="border-project">
            <v-col cols="12" md="5"> <v-img src="../assets/pics/bonbaz.jpg" class="mx-auto" max-height="300px" width="300px" @click="overlayBonbaz = !overlayBonbaz"></v-img></v-col>
            <v-overlay v-model="overlayBonbaz" class="align-center justify-center"><v-img src="../assets/pics/bonbaz-com.jpg"  height="600" width="600" @click="overlayBonbaz = !overlayBonbaz"></v-img></v-overlay>
            <v-col cols="12" md="7">
                <div>
                    <div class="text-white font-weight-bold">Front-End of Bonbaz site with react</div>
                    This site shows cost of different currencies in Iranian currency(Toman)<br />
                    this site has some features like:<br />
                    - chart for different currencies for certain period of time that user can shoose it.<br />
                    - curency converter.<br />
                    - getting export from data for other sites.<br />
                    <v-btn class="mt-5 mr-3" variant="outlined" href="https://github.com/mahiyou/bonbaz-react" width="170px"><v-icon class="mr-2">mdi-github</v-icon>source code</v-btn>
                    <v-btn class="mt-5" variant="outlined" width="170px" href="http://bonbaz.mahiyou.net"><v-icon class="mr-2">mdi-view-dashboard-outline</v-icon>live preview</v-btn>
                </div>
            </v-col>
        </v-row>
        <v-row class="border-project">
            <v-col cols="12" md="5"> <v-img src="../assets/pics/validation.jpg" class="mx-auto" max-height="300px" width="300px" @click="overlayValidation = !overlayValidation"></v-img></v-col>
            <v-overlay v-model="overlayValidation" class="align-center justify-center"><v-img src="../assets/pics/validation-com.jpg"  height="600" width="600" @click="overlayValidation = !overlayValidation"></v-img></v-overlay>
            <v-col cols="12" md="7">
                <div>
                    <div class="text-white font-weight-bold">Front-End of User Validation Form with react</div>
                    In this project Ther Is several steps for user validation: phone validation and national id validation.<br />
                    - This project is some modals and is usefull and easy to use for every site<br />
                    - In these forms, server error and validation error are handled and an appropriate message is shown to user.<br />
                    <v-btn class="mt-5 mr-3" variant="outlined" href="https://github.com/mahiyou/user-validation" width="170px"><v-icon class="mr-2">mdi-github</v-icon>source code</v-btn>
                    <v-btn class="mt-5" variant="outlined" width="170px" href="http://uservalidation.mahiyou.net"><v-icon class="mr-2">mdi-view-dashboard-outline</v-icon>live preview</v-btn>
                </div>
            </v-col>
        </v-row>
        <v-row class="border-project">
            <v-col cols="12" md="5"> <v-img src="../assets/pics/takvir.jpg" class="mx-auto" max-height="300px" width="300px" @click="overlayTakvir = !overlayTakvir"></v-img></v-col>
            <v-overlay v-model="overlayTakvir" class="align-center justify-center"><v-img src="../assets/pics/takvir-com.jpg"  height="600" width="600" @click="overlayTakvir = !overlayTakvir"></v-img></v-overlay>
            <v-col cols="12" md="7">
                <div>
                    <div class="text-white font-weight-bold">Front-End of Takvir site with vuetify</div>
                    In Takvir there is hole text of Quran(the holy book of Muslims) and voice of ayahs.<br />
                    Features:<br />
                    - Persian meaning of ayahs.<br />
                    - Ability of changing font size.<br />
                    - Several readers for each surah.<br />
                    - Ability to search.<br />
                    <v-btn class="mt-5 mr-3" variant="outlined" href="https://github.com/mahiyou/takvir-vuetify" width="170px"><v-icon class="mr-2">mdi-github</v-icon>source code</v-btn>
                    <v-btn class="mt-5" variant="outlined" width="170px" href="http://takvir.mahiyou.net"><v-icon class="mr-2">mdi-view-dashboard-outline</v-icon>live preview</v-btn>
                </div>
            </v-col>
        </v-row>
    </v-container>
</template>
<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
    data: () => ({
        tab: "all",
        overlayBonbaz: false,
        overlayTakvir: false,
        overlayDomain: false,
        overlayValidation: false,
    }),
})
</script>
<style lang="scss">
.v-container.portfolio-container {
    padding: 20px 50px;
    color: #b4b4b5;
    line-height: 30px;
    $overlay-opacity: 0.8;

    .border-project {
        border: 1px solid #56585c;
        margin-bottom: 60px;
        text-align: start;
        justify-content: end;
    }
    @media(max-width: 700px) {
        padding: 20px 20px;
    }
}
</style>
<template>
  <div class="ion-page">
    <ion-header>
      <ion-toolbar>
        <ion-title>ZipInfo PWA App</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <ZipSearch v-on:get-zip="getZipInfo"/>
      <ZipInfo v-bind:info="info"/>
      <ClearInfo v-bind:info="info" v-on:clear-info="clearInfo"/>
      <SocialContent/>
      <FooterContent/>
    </ion-content>
  </div>
</template>

<script>
// @ is an alias to /src
import ZipSearch from "../components/ZipSearch";
import ZipInfo from "../components/ZipInfo";
import SocialContent from "../components/SocialContent";
import ClearInfo from "../components/CLearInfo";
import FooterContent from "../components/FooterContent";

export default {
  name: "home",
  components: {
    ZipSearch,
    SocialContent,
    ZipInfo,
    ClearInfo,
    FooterContent
  },
  data() {
    return {
      info: null
    };
  },
  methods: {
    async getZipInfo(zip) {
      const res = await fetch(`https://api.zippopotam.us/us/${zip}`);
      if (res.status == 404) {
        this.showAlert();
      }
      this.info = await res.json();
    },
    clearInfo() {
      this.info = null;
    },
    showAlert() {
      return this.$ionic.alertController
        .create({
          header: "Not Valid",
          message: "Please enter a valid US zipcode",
          buttons: ["OK"]
        })
        .then(a => a.present());
    }
  }
};
</script>

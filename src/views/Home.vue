<template>
  <div class="ion-page">
    <ion-header>
      <ion-toolbar>
        <ion-title>ZipInfo</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
      <ZipSearch/>
      <SocialContent/>
    </ion-content>
  </div>
</template>

<script>
// @ is an alias to /src
import ZipSearch from "../components/ZipSearch";
import SocialContent from "../components/SocialContent";
export default {
  name: "home",
  components: {
    ZipSearch,
    SocialContent
  }
};
</script>

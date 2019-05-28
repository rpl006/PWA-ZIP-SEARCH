<template>
  <!-- fab placed in the center of the content with a list on each side -->
  <ion-fab vertical="center" horizontal="center" slot="fixed">
    <ion-fab-button>
      <ion-icon name="share"></ion-icon>
    </ion-fab-button>
    <ion-fab-list side="top">
      <ion-fab-button>
        <a href="https://linkedin.com">
          <ion-icon name="logo-linkedin"></ion-icon>
        </a>
      </ion-fab-button>
    </ion-fab-list>
    <ion-fab-list side="bottom">
      <ion-fab-button>
        <ion-icon name="logo-facebook"></ion-icon>
      </ion-fab-button>
    </ion-fab-list>
    <ion-fab-list side="start">
      <ion-fab-button>
        <ion-icon name="logo-instagram"></ion-icon>
      </ion-fab-button>
    </ion-fab-list>
    <ion-fab-list side="end">
      <ion-fab-button>
        <ion-icon name="logo-twitter"></ion-icon>
      </ion-fab-button>
    </ion-fab-list>
  </ion-fab>
</template>

<script>
export default {
  name: "SocialContent"
};
</script>
<style>
ion-fab {
  margin-top: 30%;
}
</style>



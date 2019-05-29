<template>
  <!-- fab placed to the top end -->
  <ion-fab vertical="bottom" horizontal="start" slot="fixed">
    <ion-fab-button>
      <ion-icon name="share"></ion-icon>
    </ion-fab-button>
    <ion-fab-list side="end">
      <ion-fab-button href="https://www.linkedin.com/in/ram-lamichhane" router-direction="root">
        <ion-icon name="logo-linkedin"></ion-icon>
      </ion-fab-button>
      <ion-fab-button href="https://m.facebook.com/rlamichhane">
        <ion-icon name="logo-facebook"></ion-icon>
      </ion-fab-button>
      <ion-fab-button href="https://github.com/rpl006">
        <ion-icon name="logo-github"></ion-icon>
      </ion-fab-button>
      <ion-fab-button href="https://twitter.com/rpl006">
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
</style>



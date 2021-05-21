<template>
  <ion-page>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>
      <div class="top">
        <img class="imgintop" src="https://viprus.co.uk/wp-content/uploads/2019/12/logo-high-res-240x300.png">
      </div>
      <div id="bg">
        <div id="main">
          <ion-button size="large" id="setup">New Viprus Link</ion-button>
        </div>
        <div class="row" id="row2">
          <ion-button id="opt" color="light"><ion-icon :icon="pricetagOutline"></ion-icon> Read<br /> Link</ion-button>
          <ion-button id="opt" color="light"><ion-icon :icon="analyticsOutline"></ion-icon> Data<br /> Sets</ion-button>
        </div>
        <div class="row" id="row3">
          <ion-button id="opt" color="light"><ion-icon :icon="informationOutline"></ion-icon>About<br />Link</ion-button>
          <ion-button id="opt" class="erase"><ion-icon :icon="trashOutline"></ion-icon>Erase<br /> Link</ion-button>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonIcon } from '@ionic/vue';
import { defineComponent } from 'vue';
import { analyticsOutline, pricetagOutline, informationOutline, trashOutline } from 'ionicons/icons';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonIcon
  },
  setup(){
    return{analyticsOutline,pricetagOutline, informationOutline, trashOutline}
  }
});
</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}
ion-icon{
  margin-right:10%;
}
.top{
  width: 100%;
  height: 42vh;
  text-align: center;
  background-color: #0093E9;
  background-image: linear-gradient(160deg, #0093E9 0%, #80D0C7 100%);
  border-radius:0px 0px 35px 35px;

}
.erase{
  --background:linear-gradient(to right, rgb(242, 112, 156), rgb(255, 148, 114));
}
.imgintop{
  text-align: center;
  object-fit:cover;
  color:black;
  width:40vw;
  transform: translateY(5vh);
}
#main{
  text-align: center;
  position: absolute;
  left: 0;
  right: 0;
  top: 42%;
  transform: translateY(-50%);
}
#container strong {
  font-size: 20px;
  line-height: 26px;
}
#opt{
  width:35vw;
  height:12vh;
  margin-inline: 4%;
  --border-radius:15px;
  text-align:right;
}
#setup{
  --border-radius:25px;
  --background:linear-gradient( 109.6deg,  rgba(62,161,219,1) 11.2%, rgba(93,52,236,1) 100.2% );

}
.row{
    text-align: center;
    --border-width:100px;
}
#row2{
  position: absolute;
  left: 0;
  right: 0;
  top: 55%;
  --border-width:100px;
}
#row3{
  position: absolute;
  left: 0;
  right: 0;
  top: 75%;
}
ion-content{
  --background: #E8E8E8;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
<template>
  <div class="link-vignette" @click="$parent.$emit('popup',{name:linkobj.name,url:linkobj.url,event:$parent.ownEvent.name})">
    <img  class="link-vignette-img"
          :style="{
            background: `linear-gradient(180deg, rgba(13, 12, 12, 0) 46.88%, #0D0C0C 100%), url(${linkobj.Image[0].url})`,
            backgroundSize: 'cover'
          }"
    />
    <span class="link-vignette-name">{{linkobj.Nom}}</span>
  </div>
</template>

<script>
export default {
  props: [
    'linkobj'
  ]
}
</script>

<style scoped>
.link-vignette {
  width: 25vw;
  margin-left: 50px;
  margin-top: 50px;
  position: relative;
  flex-shrink: 0;
  border-width: 0;
  background-color: white;
  border-radius: 20px;
  height: 260px;
}

.link-vignette-name {
  position: absolute;
  bottom: 0px;
  left: 50%;
  transform: translate(-50%,0);
  background-color: #0D0C0C;
  font-family: 'Jost';
  font-style: normal;
  font-weight: bold;
  font-size: 20px;
  line-height: 59px;
  text-align: center;
  width: calc(100% - 1px);
  color: #FFFFFF;
  border-left: solid  1px white;
  border-right: solid  1px white;
  border-bottom: solid  1px white;
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
}

.link-vignette-img {
  border-radius: 20px;
  height: 267px;
  width: 100%;
}
</style>

<template>
  <div class="cssload-loader"></div>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
</template>

<script>
export default {};
</script>

<style scoped>
.cssload-loader {
  width: 300px;
  height: 300px;
  line-height: 881px;
  margin: 294px auto;
  position: relative;
  box-sizing: border-box;
  text-align: center;
  z-index: 0;
  text-transform: uppercase;
  -o-text-transform: uppercase;
  -ms-text-transform: uppercase;
  -webkit-text-transform: uppercase;
  -moz-text-transform: uppercase;
}

.cssload-loader:before,
.cssload-loader:after {
  opacity: 0;
  box-sizing: border-box;
  -o-box-sizing: border-box;
  -ms-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  content: "\0020";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 588px;
  border: 29px solid rgb(0, 0, 0);
  box-shadow: 0 0 294px rgb(0, 0, 0), inset 0 0 294px rgb(0, 0, 0);
  -o-box-shadow: 0 0 294px rgb(0, 0, 0), inset 0 0 294px rgb(0, 0, 0);
  -ms-box-shadow: 0 0 294px rgb(0, 0, 0), inset 0 0 294px rgb(0, 0, 0);
  -webkit-box-shadow: 0 0 294px rgb(0, 0, 0), inset 0 0 294px rgb(0, 0, 0);
  -moz-box-shadow: 0 0 294px rgb(0, 0, 0), inset 0 0 294px rgb(0, 0, 0);
}

.cssload-loader:after {
  z-index: 1;
  animation: cssload-gogoloader 3.2s infinite 1.6s;
  -o-animation: cssload-gogoloader 3.2s infinite 1.6s;
  -ms-animation: cssload-gogoloader 3.2s infinite 1.6s;
  -webkit-animation: cssload-gogoloader 3.2s infinite 1.6s;
  -moz-animation: cssload-gogoloader 3.2s infinite 1.6s;
}

.cssload-loader:before {
  z-index: 2;
  animation: cssload-gogoloader 3.2s infinite;
  -o-animation: cssload-gogoloader 3.2s infinite;
  -ms-animation: cssload-gogoloader 3.2s infinite;
  -webkit-animation: cssload-gogoloader 3.2s infinite;
  -moz-animation: cssload-gogoloader 3.2s infinite;
}

@keyframes cssload-gogoloader {
  0% {
    transform: scale(0);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    transform: scale(1);
    opacity: 0;
  }
}

@-o-keyframes cssload-gogoloader {
  0% {
    -o-transform: scale(0);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    -o-transform: scale(1);
    opacity: 0;
  }
}

@-ms-keyframes cssload-gogoloader {
  0% {
    -ms-transform: scale(0);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    -ms-transform: scale(1);
    opacity: 0;
  }
}

@-webkit-keyframes cssload-gogoloader {
  0% {
    -webkit-transform: scale(0);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(1);
    opacity: 0;
  }
}

@-moz-keyframes cssload-gogoloader {
  0% {
    -moz-transform: scale(0);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    -moz-transform: scale(1);
    opacity: 0;
  }
}
</style>

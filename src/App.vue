<template>
  <div class="App">
    <div class="gradient__bg">
      <app-navbar />
      <app-header />
    </div>
    <brand />
    <what-gpt3 />
    <features />
    <possibility />
  </div>
</template>

<script>
import "./index.css";
import Navbar from "./components/Navbar/Navbar.vue";
import Header from "./components/Header.vue";
import Brand from "./components/Brand/Brand.vue";
import WhatGPT3 from "./components/WhatGPT3/WhatGPT3.vue";
import Features from "./components/Features/Features.vue";
import Possibility from "./components/Possibility.vue";

export default {
  components: {
    "app-navbar": Navbar,
    "app-header": Header,
    Brand,
    "what-gpt3": WhatGPT3,
    Features,
    Possibility
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  scroll-behavior: smooth;
}

body {
  background-color: var(--color-bg);
}

a {
  color: unset;
  text-decoration: none;
}
.gradient__bg {
  /* ff 3.6+ */
  background: -moz-radial-gradient(
    circle at 3% 25%,
    rgba(0, 40, 83, 1) 0%,
    rgba(4, 12, 24, 1) 100%
  );

  /* safari 5.1+,chrome 10+ */
  background: -webkit-radial-gradient(
    circle at 3% 25%,
    rgba(0, 40, 83, 1) 0%,
    rgba(4, 12, 24, 1) 100%
  );

  /* opera 11.10+ */
  background: -o-radial-gradient(
    circle at 3% 25%,
    rgba(0, 40, 83, 1) 0%,
    rgba(4, 12, 24, 1) 100%
  );

  /* ie 10+ */
  background: -ms-radial-gradient(
    circle at 3% 25%,
    rgba(0, 40, 83, 1) 0%,
    rgba(4, 12, 24, 1) 100%
  );

  /* global 92%+ browsers support */
  background: radial-gradient(
    circle at 3% 25%,
    rgba(0, 40, 83, 1) 0%,
    rgba(4, 12, 24, 1) 100%
  );
}
.scale-up-center {
  -webkit-animation: scale-up-center 0.4s cubic-bezier(0.39, 0.575, 0.565, 1)
    both;
  animation: scale-up-center 0.4s cubic-bezier(0.39, 0.575, 0.565, 1) both;
}

.gradient__text {
  background: var(--gradient-text);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
@-webkit-keyframes scale-up-center {
  0% {
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}
@keyframes scale-up-center {
  0% {
    -webkit-transform: scale(0.5);
    transform: scale(0.5);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}

.section__padding {
  padding: 4rem 6rem;
}

.section__margin {
  margin: 4rem 6rem;
}
@media screen and (max-width: 700px) {
  .section__margin {
    margin: 4rem;
  }

  .section__padding {
    padding: 4rem;
  }
}

@media screen and (max-width: 550px) {
  .section__margin {
    margin: 4rem 2rem;
  }

  .section__padding {
    padding: 4rem 2rem;
  }
}
</style>

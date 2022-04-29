<template>
  <div class="gpt3__features section__padding" id="features">
    <div class="gpt3__features-heading">
      <h1 class="gradient__text">
        The Future is Now and You Just Need to Realize It. Step into Future
        Today. & Make it Happen.
      </h1>
      <p>Request Early Access to Get Started</p>
    </div>
    <div class="gpt3__features-container">
      <feature
        v-for="item in featuresData"
        :title="item.title"
        :text="item.text"
        :key="item.title + index"
      />
    </div>
  </div>
</template>
<script>
import { featuresData } from "./featuresUtils";
import Feature from "../WhatGPT3/Feature.vue";
export default { data: () => ({ featuresData }), components: { Feature } };
</script>
<style>
.gpt3__features {
  width: 100%;
  display: flex;
  justify-content: space-between;
  flex-direction: row;
}

.gpt3__features-heading {
  flex: 1;
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  flex-direction: column;

  text-align: left;
  margin-right: 5rem;
}

.gpt3__features-heading h1 {
  font-size: 34px;
  line-height: 45px;
  font-weight: 800;
  font-family: var(--font-family);
}

.gpt3__features-heading p {
  color: var(--color-subtext);
  font-size: 16px;
  line-height: 30px;
  font-weight: 500;
  font-family: var(--font-family);

  margin-top: 2rem;
}

.gpt3__features-container {
  flex: 1.5;
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  flex-direction: column;
}

@media screen and (max-width: 990px) {
  .gpt3__features {
    flex-direction: column;
  }

  .gpt3__features-heading {
    margin: 0 0 2rem 0;
  }
}

@media screen and (max-width: 550px) {
  .gpt3__features-heading h1 {
    font-size: 28px;
    line-height: 38px;
  }
}
</style>

<template>
  <div class="gpt3__brand section__padding">
    <div>
      <img :src="google" alt="google" />
    </div>
    <div>
      <img :src="slack" alt="slack" />
    </div>
    <div>
      <img :src="atlassian" alt="atlassian" />
    </div>
    <div>
      <img :src="dropbox" alt="dropbox" />
    </div>
    <div>
      <img :src="shopify" alt="shopify" />
    </div>
  </div>
</template>
<script>
import { google, slack, atlassian, dropbox, shopify } from "./imports";
export default {
  data: () => ({ google, slack, atlassian, dropbox, shopify })
};
</script>
<style scoped>
.gpt3__brand {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  align-items: center;
}

.gpt3__brand div {
  flex: 1;
  max-width: 150px;
  min-width: 120px;
  margin: 1rem;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>

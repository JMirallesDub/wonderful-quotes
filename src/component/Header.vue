<template>
  <div>
    <h3>Quotes Added</h3>
    <app-form></app-form>
    <div class="progress">
      <div class="progress">
        <div
          class="progress-bar"
          role="progressbar"
          aria-valuenow="60"
          aria-valuemin="0"
          aria-valuemax="100"
          :style="{ width: (quoteCount / maxQuotes) * 100 + '%'}"
        >{{ quoteCount }} / {{ maxQuotes }}</div>
      </div>
    </div>
  </div>
</template>

<script>
import Form from "./Form";
export default {
  props: ["quoteCount", "maxQuotes"],
  components: {
    appForm: Form
  }
};
</script>

<style lang="scss" scoped>
</style>
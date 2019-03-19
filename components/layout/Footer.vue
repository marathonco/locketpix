<template>
  <footer id="footer">
    <p class="copyright">
      © {{ year }} LocketPix. All rights reserved.
    </p>
  </footer>
</template>

<script>
export default {
  computed: {
    year() {
      const currentYear = new Date().getFullYear()
      return currentYear
    }
  }
}
</script>

<style lang="scss">
#footer {
  align-items: center;
  background: getColor(background, primary);
  border-top: 4px solid getColor(background, light);
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 1rem;
  width: 100vw;
  p {
    color: getColor(text, ui);
    a {
      color: contrast-color($brand1, 20%);
      &:hover {
        color: #ffffff;
      }
    }
  }
}
</style>

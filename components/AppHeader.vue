<template>
  <div>
    <section class="masthead" role="img" aria-label="Image Description">
      <h1>
        Food App
      </h1>
      <button>
        See our restorant
      </button>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.masthead {
  // display: flex;
  // justify-content: center;
  // align-items: center;
  // flex-direction: column;
  // text-align: center;
  width: 100%;
  height: 100vh; /* if you don't want it to take up the full screen, reduce this number */
  overflow: hidden;
  background-size: cover !important;
  background: radial-gradient(
      ellipse at center,
      rgba(0, 0, 0, 0) 0%,
      rgba(0, 0, 0, 0) 67%,
      rgba(0, 0, 0, 0.65) 100%
    ),
    url(~assets/headerimg.jpg) no-repeat center center scroll;
}

h1 {
  font-style: normal;
  font-weight: bold;
  color: #eee;
  font-size: 11vmin;
  letter-spacing: 0.03em;
  line-height: 1;
  text-shadow: 1px 2px 4px rgba(0, 0, 0, 0.8);
  margin-bottom: 47px;
}

button:hover {
  background: #63b6b8;
}
button:focus {
  outline: 1px solid #fff;
  outline-offset: -4px;
}
</style>

<template>
  <main class="main px-12 py-6 d-flex flex-column justify-center">
    <h1 class="main__heading font-weight-bold mb-2">
      <transition name="typewriter">
      <span class="main__heading--primary display-4">Welcome to null</span>
      </transition>
       <br/>
      <span class="main__heading--secondary font-weight-thin">The Open Security Community</span>
      </h1>
    <h3 class="main__intro">
      We are India's largest open security community.
      <br>
      Registered as a
      non-profit society in 2010.
    </h3>
  </main>
</template>

<script>
export default {};
</script>

<style lang="scss">
.main{
  height: calc(100vh - 100px);
  align-items: flex-start;


  &__typewriter {
  font-family: monospace;
  overflow: hidden;
  white-space: nowrap;
  margin: 0 auto;
  letter-spacing: 0.17em;
  animation: typing 3.5s steps(30, end), step-end infinite;
  animation-fill-mode: forwards;
}
}

/* The typing effect */
@keyframes typing {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
}
</style>

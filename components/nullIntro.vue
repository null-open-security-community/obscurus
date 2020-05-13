<template>
  <div class>
    <div class="my-12">
      <div class="typewriter mx-auto">
        <h1 class="display-3 font-weight-bold">Welcome to null</h1>
      </div>
      <v-container>
        <v-row>
          <v-col cols="12" md="10">
            <span class="headline">
              We are India's largest open security community.
              <br/>
              Registered as a
              non-profit society in 2010.
              <br />
              Although, we've been active before that.
            </span>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.typewriter {
  font-family: monospace;
  overflow: hidden;
  white-space: nowrap;
  margin: 0 auto;
  letter-spacing: 0.17em;
  animation: typing 3.5s steps(30, end), step-end infinite;
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

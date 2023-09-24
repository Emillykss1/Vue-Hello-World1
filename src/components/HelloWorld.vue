<template>
  <div class="hello">
    <transition name="message" mode="out-in">
      <h1 v-if="showMessage" @click="toggleMessage">{{ msg }}</h1>
    </transition>
     <button class="btn" v-on:click="toggleMessage" > Mudar </button>
    <h3>Aperte no botão acima</h3>
    <h3>Vue.js</h3>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      showMessage: true
    };
  },
  methods: {
    toggleMessage() {
      this.showMessage = !this.showMessage;
    }
  }
};
</script>

<style lang="css">
.btn {
  border: none;
  padding: 0.6rem;
  border-radius: 5px;
  cursor: pointer;
  background: #03bb85;
  color: #fff

}
</style>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
<style scoped>
.hello {
  text-align: center;
  margin-top: 40px;
}

.message-enter-active,
.message-leave-active {
  transition: opacity 0.5s;
}

.message-enter, .message-leave-to /* .message-leave-active abaixo da versão 2.1.8 */ {
  opacity: 0;
}
</style>


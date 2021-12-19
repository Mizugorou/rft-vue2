<template>
  <div >
    <ef-panel id="login-page" spacing>
      <ef-loader v-if="loading"></ef-loader>
      <template v-else>
        <h1>{{ title }}</h1>
        <ef-text-field placeholder="Username"></ef-text-field>
        <ef-password-field placeholder="Password"></ef-password-field>
        <div id="button-group">
          <ef-button v-on:click="login">Login</ef-button>
          <ef-button class="test">Cancel</ef-button>
        </div>
      </template>
    </ef-panel>
  </div>
</template>

<script>
import '@refinitiv-ui/elements/lib/loader';
import '@refinitiv-ui/elements/lib/button';
import '@refinitiv-ui/elements/lib/panel';
import '@refinitiv-ui/elements/lib/text-field';
import '@refinitiv-ui/elements/lib/password-field';

export default {
  name: 'Contain',
  props: {
    msg: String
  },
  data: function() {
    return {
      title: 'Hello!',
      loading: false,
    };
  },
  methods: {
    login: function() {
      this.loading = true;

      setTimeout(() => {
        this.title = 'Done!';
        this.loading = false;
      }, 3000);
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
#login-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 450px;
  height: 200px;
  margin: 40px auto;
}

#button-group {
  margin: 10px 0;
}
</style>

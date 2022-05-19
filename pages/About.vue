<template>
  <div>
    <v-row>
      <v-col cols="12" class="text-center"><h1>About Me</h1></v-col>
      <v-col cols="12" class="text-center"><span>自己紹介</span></v-col>
    </v-row>
    <v-row class="col-md-4 offset-md-2 order-md-1">
      <v-col sm="3" md="6">
        <v-avatar left color="primary" size="72">
          <v-icon x-large>mdi-ghost</v-icon>
        </v-avatar>
      </v-col>
      <v-col sm="9" md="6">
        <ul>
          <li>1998年1月生まれ</li>
          <li>沖縄在住</li>
          <li>2022年4月~ Vue.jsの勉強を始める</li>
          <li>
            GitHub
            <a href="https://github.com/saisu18" target="_blank">@saisu18</a>
          </li>
        </ul>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
}
</script>

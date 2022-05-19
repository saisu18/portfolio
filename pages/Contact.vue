<template>
  <div>
    <v-row>
      <v-col cols="12" class="text-center"><h1>Contact</h1></v-col>
      <v-col cols="12" class="text-center"
        ><span>※モックです。実際には送信されません。</span></v-col
      >
    </v-row>
    <v-form v-model="valid">
      <v-container>
        <v-row>
          <v-col cols="12" md="7">
            <v-text-field
              v-model="firstname"
              :rules="nameRules"
              :counter="15"
              label="名前を入力してください"
              required
            ></v-text-field>
          </v-col>

          <v-col cols="12" md="7">
            <v-text-field
              v-model="email"
              :rules="emailRules"
              label="E-mailを入力してください"
              required
            ></v-text-field>
          </v-col>

          <v-col cols="12" md="7">
            <v-textarea
              v-model="message"
              :counter="150"
              label="お問い合わせ内容を入力してください"
              required
            ></v-textarea>
          </v-col>
          <v-col cols="12" md="7">
            <v-btn class="mr-4" type="submit">送信 </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-form>
  </div>
</template>

<script>
export default {
  name: 'ContactPage',
  data() {
    return {
      valid: false,
      firstname: '',
      nameRules: [
        (v) => !!v || '名前が入力されていません',
        (v) => v.length <= 15 || '15文字以内で入力してください',
      ],
      email: '',
      emailRules: [
        (v) => !!v || 'E-mailが入力されていません',
        (v) => /.+@.+/.test(v) || 'E-mailに適した入力をお願いします',
      ],
      message: '',
    }
  },
}
</script>

<style></style>

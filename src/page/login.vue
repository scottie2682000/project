<template>
  <v-card class="mx-auto my-12" max-width="374">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img
      height="250"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
    ></v-img>

    <h2 class="text-center my-2">登入</h2>

    <v-card-text>
      <v-row>
        <v-icon large color="teal darken-2 mt-2">
          mdi-email
        </v-icon>
        <v-text-field
          label="信箱"
          :rules="EmailRule"
          hide-details="auto"
        ></v-text-field>
      </v-row>
      <v-row>
        <v-icon large color="teal darken-2 mt-2">
          mdi-lock
        </v-icon>
        <v-text-field
          label="密碼"
          :rules="EmailRule"
          hide-details="auto"
        ></v-text-field>
      </v-row>
      <v-row class="flex-column mt-4">
        <v-btn depressed color="primary">
          登入
        </v-btn>
        <div>註冊</div>
      </v-row>
    </v-card-text>

    <v-divider class="mx-4"> </v-divider>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    EmailRule: [
      v => !!v || 'email is required',
      v =>
        /^\w+((-\w+)|(\.\w+))*@[A-Za-z0-9]+((\.|-)[A-Za-z0-9]+)*\.[A-Za-z]+$/.test(
          v
        ) || 'email is invalid'
    ]
  }),
  mounted() {}
}
</script>

<style></style>

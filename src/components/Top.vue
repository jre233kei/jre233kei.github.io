<template>
  <v-container>
    <v-layout text-center wrap>
      <!--
      <v-flex xs12>
        <v-img :src="require('../assets/logo.svg')" class="my-3" contain height="200"></v-img>
      </v-flex>
      -->

      <v-flex mb-4>
        <h1 class="display-2 font-weight-bold mb-3">Kota Fukui</h1>
        <p class="subheading font-weight-regular">Engineer</p>
      </v-flex>

      <v-flex mb-3>
        <h1>Skill</h1>

        <v-container fluid>
          <v-row>
            <v-col cols="12">
              <v-row
                :align="alignment"
                :justify="justify"
                class="grey lighten-5"
                style="height: 300px;"
              >
                <v-card v-for="n in 3" :key="n" class="ma-3 pa-6" outlined tile>Column</v-card>
              </v-row>
            </v-col>
            <v-col cols="12">
              <v-row justify="center">
                <v-col cols="6" md="2">
                  <v-select v-model="alignment" :items="alignmentsAvailable" label="Align"></v-select>
                </v-col>

                <v-col cols="6" md="2">
                  <v-select v-model="justify" :items="justifyAvailable" label="Justify"></v-select>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-container>
      </v-flex>

      <v-flex xs12 mb-5>
        <h2 class="headline font-weight-bold mb-3">Links</h2>
        <v-layout justify-center>
          <a
            v-for="(link, i) in links"
            :key="i"
            :href="link.href"
            class="subheading mx-3"
            target="_blank"
          >{{ link.text }}</a>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    links: [
      {
        text: 'GitHub',
        href: 'https://github.com/jre233kei/',
      },
      {
        text: 'AtCoder',
        href: 'https://atcoder.jp/users/e233',
      },
      {
        text: 'Facebook',
        href: 'https://www.facebook.com/kota.fukui.1069',
      }
    ]
  }),
};
</script>

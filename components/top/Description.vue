<template>
  <section>
    <v-layout
      column
      wrap
      class="my-5"
      align-center
    >
      <v-flex xs12 sm4 class="my-3">
        <div class="text-xs-center">
          <h2 class="headline">探し方いろいろ</h2>
          <span class="subheading">
            育児の合ってよかった！が必ず見つかる
          </span>
        </div>
      </v-flex>
      <v-flex xs12>
        <v-container grid-list-xl>
          <v-layout row wrap align-center>
            <v-flex v-for=" menu in menuItem" :key="menu.id"
                    xs12
                    md4>
              <v-hover>
                <v-card slot-scope="{ hover }"
                        :class="`elevation-${hover ? 12 : 2}`"
                        class="elevation-0 transparent"
                        href="{ menu.href }">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="blue--text text--lighten-2">{{ menu.icon }}</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">{{ menu.headline }}</div>
                  </v-card-title>
                </v-card>
              </v-hover>
            </v-flex>
          </v-layout>
        </v-container>
      </v-flex>
    </v-layout>
  </section>
</template>

<script>
export default {
  name: 'Description',
  data() {
    return {
      menuItem: [
        {
          icon: 'face',
          headline: '月齢から探す',
          href: '/category'
        },
        {
          icon: 'view_list',
          headline: 'カテゴリから探す',
          href: '/category'
        },
        {
          icon: 'note',
          headline: 'グッズの紹介記事を読む',
          href: '/category'
        }
      ]
    }
  }
}
</script>

<style scoped>
</style>

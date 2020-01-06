<template>
  <mdb-container>
    <mdb-row class="my-5">
      <mdb-card-group deck>
        <mdb-card>
          <mdb-card-body>
            <mdb-card-title>Demo 1</mdb-card-title>
            <mdb-card-text>
              three.js + Typescript + Vue.js集成测试
            </mdb-card-text>
          </mdb-card-body>
          <mdb-card-footer>
            <mdb-btn color="primary" @click="goTo('demo1')">
              <mdb-icon fab icon="vuejs" class="mr-2" />进入
            </mdb-btn>
          </mdb-card-footer>
        </mdb-card>

        <mdb-card>
          <mdb-card-body>
            <mdb-card-title>Demo 2</mdb-card-title>
            <mdb-card-text>
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </mdb-card-text>
          </mdb-card-body>
          <mdb-card-footer>
            <mdb-btn color="primary">
              进入
            </mdb-btn>
          </mdb-card-footer>
        </mdb-card>

        <mdb-card>
          <mdb-card-body>
            <mdb-card-title>Demo 3</mdb-card-title>
            <mdb-card-text>
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </mdb-card-text>
          </mdb-card-body>
          <mdb-card-footer>
            <mdb-btn color="primary">
              进入
            </mdb-btn>
          </mdb-card-footer>
        </mdb-card>
      </mdb-card-group>
    </mdb-row>

    <mdb-row>
      <mdb-card-group deck>
        <mdb-card>
          <mdb-card-body>
            <mdb-card-title>Demo 1</mdb-card-title>
            <mdb-card-text>
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </mdb-card-text>
          </mdb-card-body>
          <mdb-card-footer>
            <mdb-btn color="primary">
              进入
            </mdb-btn>
          </mdb-card-footer>
        </mdb-card>

        <mdb-card>
          <mdb-card-body>
            <mdb-card-title>Demo 2</mdb-card-title>
            <mdb-card-text>
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </mdb-card-text>
          </mdb-card-body>
          <mdb-card-footer>
            <mdb-btn color="primary">
              进入
            </mdb-btn>
          </mdb-card-footer>
        </mdb-card>

        <mdb-card>
          <mdb-card-body>
            <mdb-card-title>Demo 3</mdb-card-title>
            <mdb-card-text>
              Some quick example text to build on the card title and make up the
              bulk of the card's content.
            </mdb-card-text>
          </mdb-card-body>
          <mdb-card-footer>
            <mdb-btn color="primary">
              进入
            </mdb-btn>
          </mdb-card-footer>
        </mdb-card>
      </mdb-card-group>
    </mdb-row>
  </mdb-container>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

@Component
export default class App extends Vue {
  private goTo (routeName: string) {
    this.$router.push({ name: routeName })
  }
}
</script>

<style>
.container {
  min-height: 100vh;
}
</style>

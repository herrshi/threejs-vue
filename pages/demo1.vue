<template>
  <div id="container" />
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
import * as Three from 'three'

@Component
export default class Demo1 extends Vue {
  camera!: Three.Camera
  scene!: Three.Scene
  renderer!: Three.Renderer
  mesh!: Three.Mesh

  mounted () {
    this.init()
    this.animate()
  }

  private init () {
    const container = document.getElementById('container') as HTMLElement

    this.camera = new Three.PerspectiveCamera(
      70,
      container.clientWidth / container.clientHeight,
      0.01
    )
    this.camera.position.z = 1

    this.scene = new Three.Scene()

    const geometry = new Three.BoxGeometry(0.2, 0.2, 0.2)
    const material = new Three.MeshNormalMaterial()

    this.mesh = new Three.Mesh(geometry, material)
    this.scene.add(this.mesh)

    this.renderer = new Three.WebGLRenderer({ antialias: true })
    this.renderer.setSize(container.clientWidth, container.clientHeight)
    container.appendChild(this.renderer.domElement)
  }

  private animate () {
    requestAnimationFrame(this.animate)
    this.mesh.rotation.x += 0.01
    this.mesh.rotation.y += 0.02
    this.renderer.render(this.scene, this.camera)
  }
}
</script>

<style scoped>
#container {
  height: 100vh;
}
</style>



<template>
  <div class="canvas-container">

    <Suspense>
      <TresCanvas style="width: 100%; height: 550px;">
        <OrbitControls />
        <TresPerspectiveCamera :position="[5, 5, 5]" :fov="1.2" :near="0.1" :far="1000" />
        <TresScene>
          <TresMesh v-bind="scene" />
          <TresDirectionalLight :position="[5, 5, 5]" :intensity="70" />
        </TresScene>
      </TresCanvas>

    </Suspense>
  </div>
</template>
<script setup lang="ts">


import { ref } from 'vue';
import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader';

import { useLoader } from '@tresjs/core';
import { OrbitControls, GLTFModel } from '@tresjs/cientos';


const meshPosition = [0, 3, 0];

const lightRef = ref(null);

const { scene } = await useLoader(
  GLTFLoader,
  'https://raw.githubusercontent.com/WeslleyJs/arno/main/scene.gltf'
);
</script>
<style></style>
<script setup lang="ts">
import { BasicShadowMap, SRGBColorSpace, NoToneMapping } from 'three';
import { OrbitControls, Text3D } from '@tresjs/cientos';
// Orbit controls by extending

const gl = {
  clearColor: '#82DBC5',
  shadows: true,
  alpha: false,
  shadowMapType: BasicShadowMap,
  outputColorSpace: SRGBColorSpace,
  toneMapping: NoToneMapping,
};
</script>

<template>
  <TresCanvas v-bind="gl" window-size>
    <TresPerspectiveCamera :position="[4, 3, 9]" />
    <OrbitControls />
    <Suspense>
      <Text3D
        :position="[0, 1, 0]"
        text="naito.dev"
        font="https://raw.githubusercontent.com/Tresjs/assets/main/fonts/FiraCodeRegular.json" 
      >
        <TresMeshNormalMaterial />
      </Text3D>
    </Suspense>
    <TresDirectionalLight :position="[0, 2, 4]" :intensity="1.2" cast-shadow />
    <TresGridHelper />
    <TresAxesHelper :args="[5]"/>
  </TresCanvas>
</template>

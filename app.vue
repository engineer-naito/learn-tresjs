<template>
  <TresCanvas window-size clear-color="#82DBC5">
    <TresMesh>
      <TresBoxGeometry :args="[1,2,3]"/>
      <TresMeshNormalMaterial />
    </TresMesh>
  </TresCanvas>
</template>

<template>
  <TresCanvas window-size clear-color="#000000">
    <TresPerspectiveCamera 
      :position="[5, 5, 5]"
      :look-at="[0, 0, 0]"
    />
    <TresMesh 
      :position="[0, 2, 0]"
    >
      <TresBoxGeometry />
      <TresMeshStandardMaterial color="white" />
    </TresMesh>
    <TresAmbientLight :args="['white', 2]" />
    <TresDirectionalLight
      :position="[2, 0, 0]"
      :color="'purple'"
      :intensity="8"
    />
    <TresAxesHelper :args="[5]" />
  </TresCanvas>
</template>

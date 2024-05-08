<script setup lang="ts">
  import * as THREE from 'three'
  import { TresCanvas } from '@tresjs/core';
  import { shallowRef } from 'vue';
  // const sense = new THREE.Scene();
  // const geometry = new THREE.TorusGeometry(1, 0.5 ,16, 32)
  // const material = new THREE.MeshBasicMaterial({ color: 'green' });
  // const donut = new THREE.Mesh(geometry, material);
  // sense.add(donut);
  const green = new THREE.Color('orange');
  const cameraPosition = new THREE.Vector3(3, 3, 3);
  const lookAtPosition = new THREE.Vector3(0, 0, 0);
</script>

<template>
  <TresCanvas clear-color="#82DBC5" window-size>
    <TresPerspectiveCamera :position="cameraPosition" :look-at="lookAtPosition" />
    <TresMesh>
      <TresTorusGeometry :arg="[1, 0.5, 16, 32]" />
      <TresMeshBasicMaterial :color="green" />
    </TresMesh>
    <TresAmbientLight :intensity="1" />
  </TresCanvas>
</template>

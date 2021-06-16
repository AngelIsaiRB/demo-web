<template>
  <div class="w-screen h-screen absolute top-0">
      <div class="w-full h-full " id="globe">

      </div>
  </div>
</template>

<script>
import * as THREE from "three"
export default {
mounted () {
const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera( 75, document.querySelector('#globe').clientWidth / document.querySelector('#globe').clientHeight, 0.1, 1000 );

const renderer = new THREE.WebGLRenderer({ alpha: true });

renderer.setSize( document.querySelector('#globe').clientWidth, document.querySelector('#globe').clientHeight );
document.querySelector('#globe').appendChild( renderer.domElement );
const geometry = new THREE.SphereGeometry( 2, 10, 10 );
const material = new THREE.MeshBasicMaterial( {color: 0x002F58,wireframe:true} );
const cube = new THREE.Mesh( geometry, material );
scene.add( cube );
scene.background

camera.position.z = 5;
camera.position.x = -3;
window.addEventListener( 'resize', onWindowResize, false );
function onWindowResize(){
    camera.aspect = document.querySelector('#globe').clientWidth / document.querySelector('#globe').clientHeight;
    camera.updateProjectionMatrix();
    renderer.setSize( document.querySelector('#globe').clientWidth , document.querySelector('#globe').clientHeight );

}

function animate() {
	requestAnimationFrame( animate );
	renderer.render( scene, camera );
    cube.rotation.y += 0.005;
}
onWindowResize();
animate();
},
}
</script>

<style>

</style>
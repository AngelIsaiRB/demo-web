<template>
  <div class="w-screen h-screen absolute top-0">
      <div class="w-full h-full " id="ddd">

      </div>
  </div>
</template>

<script>
import * as THREE from "three"
export default {
mounted () {

			let camera, scene, renderer, clock;

			init();
			animate();

			function init() {

				const container = document.createElement( 'div' );
				document.querySelector('#ddd').appendChild( container );

				camera = new THREE.PerspectiveCamera( 60, document.querySelector('#ddd').clientWidth / document.querySelector('#ddd').clientHeight, 0.1, 10 );
				camera.position.set( 0, 0, 1 );

				clock = new THREE.Clock();

				scene = new THREE.Scene();

				const colorArray = [ new THREE.Color( 0xff0080 ), new THREE.Color( 0xffffff ), new THREE.Color( 0x8000ff ) ];
				const positions = [];
				const colors = [];

				for ( let i = 0; i < 100; i ++ ) {

					positions.push( Math.random() - 0.5, Math.random() - 0.5, Math.random() - 0.5 );

					const clr = colorArray[ Math.floor( Math.random() * colorArray.length ) ];

					colors.push( clr.r, clr.g, clr.b );

				}

				const geometry = new THREE.BufferGeometry();
				geometry.setAttribute( 'position', new THREE.Float32BufferAttribute( positions, 3 ) );
				geometry.setAttribute( 'color', new THREE.Float32BufferAttribute( colors, 3 ) );

				const material = new THREE.PointsMaterial( { size: 4, vertexColors: true, depthTest: false, sizeAttenuation: false } );

				const mesh = new THREE.Points( geometry, material );
				scene.add( mesh );

				renderer = new THREE.WebGLRenderer( { preserveDrawingBuffer: true } );
				renderer.setPixelRatio( window.devicePixelRatio );
				renderer.setSize( document.querySelector('#ddd').clientWidth, document.querySelector('#ddd').clientHeight );
				renderer.autoClearColor = false;
				container.appendChild( renderer.domElement );

				//

				window.addEventListener( 'resize', onWindowResize );

			}

			function onWindowResize() {

				camera.aspect = document.querySelector('#ddd').clientWidth / document.querySelector('#ddd').clientHeight;
				camera.updateProjectionMatrix();

				renderer.setSize( document.querySelector('#ddd').clientWidth, document.querySelector('#ddd').clientHeight );

			}

			//

			function animate() {

				requestAnimationFrame( animate );

				render();

			}

			function render() {

				const elapsedTime = clock.getElapsedTime();

				scene.rotation.y = elapsedTime * 0.5;

				renderer.render( scene, camera );

			}
},
}
</script>

<style>

</style>
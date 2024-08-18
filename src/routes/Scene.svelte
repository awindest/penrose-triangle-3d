<script lang="ts">
	import { T } from '@threlte/core'
	import { Environment, OrbitControls } from '@threlte/extras'
	import PenroseTriangle from './Penrose_triangle.svelte';
</script>

<T.PerspectiveCamera
	makeDefault
	fov={10}
	position={[0, 0, 70]}
>
	<OrbitControls
		autoRotate={true}
		autoRotateSpeed={0.4}
		enableZoom={true}
	/>

</T.PerspectiveCamera>

<Environment files="/oil-on-water.png" /> // this image maps to the model surface otherwise it would be black

<PenroseTriangle />

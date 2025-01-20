<template>
 <div class="dot">
  <MyCertificate />
 </div>
</template>

<script>
import MyCertificate from './components/MyCertificate.vue'


export default {
  name: 'App',
  components: {
    
    MyCertificate,
  
  }
}
</script>

<style>
@import './style.css';
	.dot{
    animation: gradient-move 15s linear infinite;
    background-image: linear-gradient(to bottom, transparent, transparent 20%, #fff 20%),
			linear-gradient(to right, #000, #000 20%, #fff 20%);
		background-size: 3px 3px;
	}
</style>

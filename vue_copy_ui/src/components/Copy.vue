<template>
  <div class="center content-inputs">
    <vs-input v-model="input_value" placeholder="Type something..."/>
		<vs-button
      shadow
      :active="active == 1"
      @click="doCopy();"
    >
		Copy
    </vs-button>
		<p></p>
	</div>
</template>

<script>
  export default {

		data(){
			return {
				input_value: '',
				active: 0
			}
		},
		
		methods:{
			animation: function () {
				this.active = 1;
				this.active = 0;
			},
			doCopy: function () {
				navigator.clipboard.writeText(this.input_value);
			},
			
		}
  }
</script>

<style>
.center {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  /* height: 100vh; */
}
</style>
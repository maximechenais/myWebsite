<template>
	<div>
		<div class="top">
			<topbar />
			<planetStars />
		</div>
		<div class="content">
			<menuNavigation />         
			<Nuxt />
		</div>
		<!-- <div class="point-star" v-show="isLight"></div> -->
	</div>
</template>

<script>
import topbar from '@/components/topbar/topbar'
import planetStars from '@/components/topbar/planet'
import menuNavigation from '@/components/menu/menu'

export default {
	components: {
		topbar,
		planetStars,
		menuNavigation
	},

	data() {
		return {
			isLight: true,
		}
	},

	// mounted() {
	// 	this.switchOnStar()
	// },

	// methods: {
	// 	switchOnStar() {
	// 		this.isLight = true
	// 		if (this.isLight) {
	// 			console.log('coucou')
	// 		}
	// 	},
	// 	switchOffStar() {
	// 		this.isLight = false
	// 	}
	// }
}
</script>

<style>
	body {
		height: 100vh;
		max-width: 100vw;
		margin: 0;
		background-color: #291B25;
		background-image: url(../assets/background/mountains.svg);
		background-repeat: repeat-x;
		background-position: bottom;
	}
	html {
		font-family: 'Montserrat';
	}

	.top {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
	}

	.point-star {
		height: 50px;
		width: 50px;
		border-radius: 50%;
		background-color: white;
	}

	.content {
		display: flex;
		flex-direction: row;
	}
</style>

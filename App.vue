<script>
	export default {
		onLaunch: function() {
			console.log('打算这里用全局globalData获取屏幕高度,但是得出来的比单个页面的高一点点')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		},
	}
</script>

<style lang="scss">
	/*每个页面公共css */
	@import "uview-ui/index.scss";
	@import "uni.scss";
	@import "common/common.scss";
	@import "common/home/home.scss";
</style>

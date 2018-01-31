<template>

<div>

        <wxc-minibar background-color="#3eb4ff">
            <image src="https://img.alicdn.com/tfs/TB1QN8pdlHH8KJjy0FbXXcqlpXa-220-80.png"
                   slot="left"
                   style="height: 32px;width: 88px;"></image>
            <text style="font-size: 40px;" slot="middle">CCTV.COM-UC</text>
            <image slot="right"
                   src="https://img.alicdn.com/tfs/TB1j39Uc0fJ8KJjy0FeXXXKEXXa-160-128.png"
                   style="height: 32px;width: 40px"></image>
        </wxc-minibar>
    <div class="wrapper">
        <image :src="logo" class="logo"></image>
        <text class="greeting">CCTV.com</text>
    </div>
</div>
</template>

<script>
    import {WxcMinibar} from  'weex-ui';
//    const modal = weex.requireModule('modal');
    export default {
        components: { WxcMinibar },
        data () {
            return {
                logo: 'https://gw.alicdn.com/tfs/TB1yopEdgoQMeJjy1XaXXcSsFXa-640-302.png',
            }
        }
    }
</script>

<style scoped>
    .wrapper {
        justify-content: center;
        align-items: center;
    }

    .logo {
        width: 424px;
        height: 200px;
    }

    .greeting {
        margin-top: 70px;
        font-size: 50px;
        color: #41B883;
    }

    .message {
        margin: 30px;
        font-size: 32px;
        color: #727272;
    }
</style>

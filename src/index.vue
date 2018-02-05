<template>
    <div>

        <wxc-tab-bar :tab-titles="tabIconFontTitles" :tab-styles="tabIconFontStyles" title-type="iconFont">
            <!-- 第一个页面内容-->
            <div class="item-container" :style="contentStyle">
                <wxc-minibar background-color="#3eb4ff" leftButton="">
                    <text style="font-size: 40px;" slot="middle">通行证</text>
                </wxc-minibar>


                <passport></passport>
            </div>

            <!-- 第二个页面内容-->
            <div class="item-container" :style="contentStyle">
                <wxc-minibar background-color="#3eb4ff" leftButton="">
                    <text style="font-size: 40px;" slot="middle">用户中心</text>
                </wxc-minibar>

                <usercenter></usercenter>
            </div>

            <!-- 第三个页面内容-->
            <div class="item-container" :style="contentStyle">
                <wxc-minibar background-color="#3eb4ff" leftButton="">
                    <text style="font-size: 40px;" slot="middle">推荐系统</text>
                </wxc-minibar>
                <recommend></recommend>
            </div>

            <!-- 第四个页面内容-->
            <div class="item-container" :style="contentStyle">
                <wxc-minibar background-color="#3eb4ff" leftButton="">
                    <text style="font-size: 40px;" slot="middle">设置中心</text>
                </wxc-minibar>
                <setting></setting>
            </div>
        </wxc-tab-bar>
    </div>
</template>

<script>
    import {WxcMinibar, WxcTabBar} from  'weex-ui';
    import Passport from './views/passport';
    import Usercenter from "./views/usercenter";
    import Recommend from "./views/recommend";
    import Setting from "./views/setting";

    export default {
        components: {
            Setting,
            Recommend,
            Usercenter,
            Passport,
            WxcMinibar, WxcTabBar
        },
        data () {
            return {
                tabIconFontTitles: [
                    {
                        title: '通行证',
                        codePoint: '\ue604',
                    }, {
                        title: '用户中心',
                        codePoint: '\ue613',
                    }, {
                        title: '推荐系统',
                        codePoint: '\ue603',
                    }, {
                        title: '其它设置',
                        codePoint: '\ue608'
                    }],
                tabIconFontStyles: {
                    bgColor: '#FFFFFF',
                    titleColor: '#666666',
                    activeTitleColor: '#3D3D3D',
                    activeBgColor: '#FFFFFF',
                    isActiveTitleBold: true,
                    width: 160,
                    height: 120,
                    fontSize: 24,
                    textPaddingLeft: 10,
                    textPaddingRight: 10,
                    iconFontSize: 50,
                    iconFontColor: '#333333',
                    activeIconFontColor: 'red',
                    iconFontUrl: '//at.alicdn.com/t/font_555238_o9p1c2w06tsdobt9.ttf'
                }
            }
        },
        methods: {
            contentStyle(){

            }
        }
    }
</script>

<style scoped>
</style>

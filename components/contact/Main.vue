<template>
    <section class="flexView">
        <Header/>
            <section class="scrollView">
                <Search/>
                <Group/>
                <div class="divHeight"></div>  <!-- 换行空格 -->
                <Enterprice/>
                <div class="divHeight"></div>   <!-- 换行空格 -->
                <Cmmonly/>
            </section>
        <Footer/>
    </section>

</template>

<script>
import Header from './Header.vue'
import Search from './Search.vue'
import Group from './Group.vue'
import Enterprice from './Enterprice.vue'
import Cmmonly from './Cmmonly.vue'
import Footer from './Footer.vue'
export default {
    components:{Header,Search,Group,Enterprice,Cmmonly,Footer},
    mounted(){
        // 存储数据
        window.localStorage.setItem('Items',JSON.stringify(
            [
                {
                    id:'001',
                    title:'我的部门',
                    imgurl:'/images/nav-005.png',
                    to:'https://www.baidu.com'
                },
                {
                    id:'002',
                    title:'公司团队',
                    imgurl:'/images/nav-006.png',
                    to:'https://www.baidu.com'
                }
            ]))
        window.localStorage.setItem('Persons',JSON.stringify([
                {
                    id:'001',
                    name:'张三',
                    lastmessage:'什么时候可以完成这个项目啊',
                    imgurl:'/images/user-logo-001.png',
                    lastseen:'昨天',
                    to:'https:/baidu.com?id=001&name=张三',
                    
                },
                {
                    id:'002',
                    name:'夏红',
                    lastmessage:'今天晚上静默要上线',
                    imgurl:'/images/user-logo-002.png',
                    lastseen:'星期一',
                    to:'https:/baidu.com?id=002&name=夏红',
                    
                },
                {
                    id:'003',
                    name:'设计师小红',
                    lastmessage:'今天晚上静默要上线',
                    imgurl:'/images/user-logo-003.png',
                    lastseen:'星期一',
                    to:'https:/baidu.com?id=003&name=设计师小红',
                    
                },
                {
                    id:'004',
                    name:'张洢豪',
                    lastmessage:'今天晚上静默要上线',
                    imgurl:'/images/user-logo-004.png',
                    lastseen:'星期一',
                    to:'https:/baidu.com?id=004&name=张洢豪',
                    
                }
            ]))
    }
}
</script>

<style>
    html, body {
    color: #333;
    margin: 0;
    height: 100%;
    font-family: "Myriad Set Pro", "Helvetica Neue", Helvetica, Arial, Verdana, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-weight: normal;
}
* {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}
a {
    text-decoration: none;
    color: #000;
}
a, label, button, input, select {
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
img {
    width: 100%;
    height: auto;
    display: block;
    border: 0;
}
body {
    background: #f4f4f4;
    color: #666;
}
html, body, div, dl, dt, dd, ol, ul, li, h1, h2, h3, h4, h5, h6, p, blockquote, pre, button, fieldset, form, input, legend, textarea, th, td {
    margin: 0;
    padding: 0;
}
a {
    text-decoration: none;
    color: #08acee;
}
button {
    outline: 0;
}
img {
    border: 0;
}
button, input, optgroup, select, textarea {
    margin: 0;
    font: inherit;
    color: inherit;
    outline: none;
}
li {
    list-style: none;
}
a {
    color: #666;
}
.clearfix::after {
    clear: both;
    content: ".";
    display: block;
    height: 0;
    visibility: hidden;
}
.clearfix {
}
.divHeight {
    width: 100%;
    height: 10px;
    background: #f5f5f5;
    position: relative;
    overflow: hidden;
}
.r-line {
    position: relative;
}
.r-line:after {
    content: '';
    position: absolute;
    z-index: 0;
    top: 0;
    right: 0;
    height: 100%;
    border-right: 1px solid #D9D9D9;
    -webkit-transform: scaleX(0.5);
    transform: scaleX(0.5);
    -webkit-transform-origin: 100% 0;
    transform-origin: 100% 0;
}
.b-line {
    position: relative;
}
.b-line:after {
    content: '';
    position: absolute;
    z-index: 2;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 1px;
    border-bottom: 1px solid #e2e2e2;
    -webkit-transform: scaleY(0.5);
    transform: scaleY(0.5);
    -webkit-transform-origin: 0 100%;
    transform-origin: 0 100%;
}
.arrow {
    position: relative;
    padding-right: 0.8rem;
}
.arrow span {
    font-size: 0.8rem;
    color: #9b9b9b;
}
.arrow:after {
    content: " ";
    display: inline-block;
    height: 6px;
    width: 6px;
    border-width: 2px 2px 0 0;
    border-color: #848484;
    border-style: solid;
    -webkit-transform: matrix(0.71, 0.71, -0.71, 0.71, 0, 0);
    transform: matrix(0.71, 0.71, -0.71, 0.71, 0, 0);
    position: relative;
    top: -2px;
    position: absolute;
    top: 50%;
    margin-top: -4px;
    right: 2px;
    border-radius: 1px;
}
.flex {
    display: -webkit-box;
    display: -webkit-flex;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    align-items: center;
    padding: 15px;
    position: relative;
}
.flex-box {
    -webkit-box-flex: 1;
    -webkit-flex: 1;
    flex: 1;
    min-width: 0;
    font-size: 14px;
    color: #333;
}
/* 必要布局样式css */

.flexView {
    width: 100%;
    height: 100%;
    margin: 0 auto;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -webkit-flex-direction: column;
    -ms-flex-direction: column;
    flex-direction: column;
}
.scrollView {
    width: 100%;
    height: 100%;
    -webkit-box-flex: 1;
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    overflow-y: auto;
    overflow-x: hidden;
    -webkit-overflow-scrolling: touch;
    position: relative;
    padding-bottom: 50px;
}
.navBar {
    height: 44px;
    position: relative;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    z-index: 102;
    background: #00aaf2;
}
.navBar-item {
    height: 44px;
    min-width: 25%;
    -webkit-box-flex: 0;
    -webkit-flex: 0 0 25%;
    -ms-flex: 0 0 25%;
    flex: 0 0 25%;
    padding: 0 0.9rem;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    font-size: 0.7rem;
    white-space: nowrap;
    overflow: hidden;
    color: #808080;
    position: relative;
}
.navBar-item:first-child {
    -webkit-box-ordinal-group: 2;
    -webkit-order: 1;
    -ms-flex-order: 1;
    order: 1;
    margin-right: -25%;
    font-size: 0.7rem;
    color: #fff;
}
.navBar-item:last-child {
    -webkit-box-ordinal-group: 4;
    -webkit-order: 3;
    -ms-flex-order: 3;
    order: 3;
    -webkit-box-pack: end;
    -webkit-justify-content: flex-end;
    -ms-flex-pack: end;
    justify-content: flex-end;
}
.center {
    -webkit-box-ordinal-group: 3;
    -webkit-order: 2;
    -ms-flex-order: 2;
    order: 2;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: center;
    -webkit-justify-content: center;
    -ms-flex-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    height: 44px;
    width: 50%;
    margin-left: 25%;
}
.center-title {
    text-align: center;
    width: 100%;
    white-space: nowrap;
    overflow: hidden;
    display: block;
    text-overflow: ellipsis;
    font-size: 0.95rem;
    color: #fff;
}
.icon {
    width: 20px;
    height: 20px;
    display: block;
    border: none;
    float: left;
    background-size: 20px;
    background-repeat: no-repeat;
}
.icon-return {
    background-image: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAACh0lEQVRoQ+3ZMW8TMRQH8PcOsTBQISExVCIRCwgWFvZ+hZYBpIrEcTYkBsTGlI2VDamL3YEBpWJoR1BJaOlXYEzyDYp0bMRGRjnJoDuWs/1e3EbKeHf55b33vzsb4YJ98IJ54RKce8XZV1gIcQ8AviDiD2vtC631pzZFYQ2WUt611p4CwM0VcqqU2soSXIN1ztdKqTfZgRuw75RSz9tg3bHsWjomlh04NpYVOAWWDbjf7z8oimLipbH7bUopJdvO7L/Hk8+wwyLiCSLe8H6cww4BwGYFTo0lbWkKLBmYCksCrsNaa99rrZ/FmFnS0GrCdrvd3mg0MqEDqu58yVKaAzZZSwshHgLAsX/rcW2csrJVtaNXeIWdIuL16qJU2OgVrsMCwEGn03mSamaThVYTtizLp+PxeJkioJKFFldslJbmjA0O5o4NCm7AHpZluUM5s1FCSwjxCAA++7ceADiczWaPJ5PJL6qAihJaUspdY8w+Il7xLsASG6SlhRA/EfGa91BxNJ/Pd7hVNtiT1mAwOAeADXdCa637Hi0Wi3zBUsptY8wHRLzqwIh/nlbzbWmna0roLEOrmo11QQd9W1oHdFDwOrR3cLCH/uuFn0uQRQE7dMPKJHl6RwNzRUcF/w9N9VIRHVyhazbLDihWP5KAHbphOzQ5OhmYCzopmAM6OZgaTQL20FMAuOUtHESfaTLwCn3HWnuWEk0KpkCTg1OjWYArtDHmKyJu+jMdeh+KDdghh8NhZ7lcfvPRoXcaWYFToNmBY6NZgj20m+nb3pr3W631yzY7GWzBDtXr9TaLojjz0N+VUvezBXvoPQBw0Fda649Zg9vg6o5l3dKhse58l+AY/yqnc/4GvNDoTFOq8FwAAAAASUVORK5CYII=");
}
.m-slider {
    overflow-x: hidden;
    width: 100%;
    position: relative;
}
.slider-wrapper {
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    width: 100%;
    height: 100%;
    -webkit-transform: translate3d(0px, 0px, 0px);
    transform: translate3d(0px, 0px, 0px);
    position: relative;
    z-index: 1;
    -webkit-transition-property: -webkit-transform;
    transition-property: -webkit-transform;
    transition-property: transform;
    transition-property: transform, -webkit-transform;
}
.slider-item {
    width: 100%;
    height: 100%;
    -webkit-flex-shrink: 0;
    -ms-flex-negative: 0;
    flex-shrink: 0;
    background: #f6f6f6;
}
.slider-item img {
    width: 100%;
    height: auto;
    display: block;
    border: none;
}
.slider-pagination {
    text-align: right;
    position: absolute;
    width: 100%;
    z-index: 2;
    right: 0;
    bottom: 10px;
    pointer-events: none;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: end;
    -webkit-align-items: flex-end;
    -ms-flex-align: end;
    align-items: flex-end;
    -webkit-box-pack: center;
    -webkit-justify-content: center;
    -ms-flex-pack: center;
    justify-content: center;
}
.slider-pagination > .slider-pagination-item {
    margin: 0 .25rem;
    width: 8px;
    height: 8px;
    display: inline-block;
    border-radius: 100%;
    background-color: rgba(255,255,255,0.4);
}
.slider-pagination > .slider-pagination-item.slider-pagination-item-active {
    background-color: #fff;
    border-radius: 100%;
}
.palace {
    padding: 0.5rem 0;
    position: relative;
    overflow: hidden;
}
.palace-grid {
    position: relative;
    float: left;
    padding: 1px;
    width: 20%;
    box-sizing: border-box;
    margin: 5px 0;
}
.palace-grid-icon {
    width: 30px;
    height: 30px;
    margin: 0 auto;
}
.palace-grid-icon img {
    display: block;
    width: 100%;
    height: 100%;
    border: none;
}
.palace-grid-text {
    display: block;
    text-align: center;
    color: #333;
    font-size: 0.85rem;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
    padding-top: 0.2rem;
}
.palace-grid-text h2 {
    font-size: 0.8rem;
    font-weight: normal;
    color: #666666;
}
.m-actionsheet {
    text-align: center;
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
    background-color: #EFEFF4;
    -webkit-transform: translate(0, 100%);
    transform: translate(0, 100%);
    -webkit-transition: -webkit-transform .3s;
    transition: -webkit-transform .3s;
    transition: transform .3s;
    transition: transform .3s, -webkit-transform .3s;
}
.mask-black {
    background-color: rgba(0, 0, 0, 0.4);
    position: fixed;
    z-index: 500;
    bottom: 0;
    right: 0;
    left: 0;
    top: 0;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-pack: center;
    -webkit-justify-content: center;
    -ms-flex-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    z-index: 998;
}
.actionsheet-action {
    display: block;
    margin-top: .15rem;
    font-size: 0.28rem;
    color: #555;
    height: 1rem;
    line-height: 1rem;
    background-color: #FFF;
}
.m-actionsheet {
    text-align: center;
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    z-index: 10005;
    background-color: #ffffff;
    -webkit-transform: translate(0, 100%);
    transform: translate(0, 100%);
    -webkit-transition: -webkit-transform .3s;
    transition: -webkit-transform .3s;
    transition: transform .3s;
    transition: transform .3s, -webkit-transform .3s;
}
.actionsheet-toggle {
    -webkit-transform: translate(0, 0);
    transform: translate(0, 0);
}
.actionsheet-item {
    display: block;
    position: relative;
    font-size: 0.85rem;
    color: #555;
    height: 2rem;
    line-height: 2rem;
    background-color: #FFF;
}
.actionsheet-item {
    display: block;
    position: relative;
    font-size: 0.85rem;
    color: #555;
    height: 2rem;
    line-height: 2rem;
    background-color: #FFF;
}
.coll-cancel a {
    height: 45px;
    line-height: 45px;
    font-size: 12px;
    background: #f9f9f9;
    display: block;
    text-align: center;
    width: 100%;
}
.coll-share-img {
    width: 38px;
    height: 38px;
    margin: 0 auto;
}
.coll-share-img img {
    width: 100%;
    height: auto;
    display: block;
    border: none;
}
.coll-share-box {
    position: relative;
    overflow: hidden;
    padding: 10px 0;
}
.coll-cancel a {
    height: 45px;
    line-height: 45px;
    font-size: 12px;
    background: #f9f9f9;
    display: block;
    text-align: center;
    width: 100%;
}
.coll-share-item {
    position: relative;
    float: left;
    padding: 8px 10px;
    width: 33.333%;
    box-sizing: border-box;
    font-size: 12px;
    height: 85px;
}
.rule {
    position: absolute;
    right: 0;
    top: 1rem;
    background: #54ca9a;
    border-radius: 50px 0 0 50px;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
    color: #fff;
}
.icon-add {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAFT0lEQVRoQ+2aj7EXNRCAsxWoFQgVCBWIFagVCBWgFagVCBUIFQgVCBUIFQgVoBWs8zGbN/nlNtncXfIYeGbmNzzmcrl82b/ZRNINa3LDeNP/wJ+6xJdKWFVvpZS+TSndSyl9bovJ32V7k1LiR3uVUnomIi9XLfx0YFW9Y5DfpZT4+0j7B3D7vRQR/j+lTQM20N9MmlMmZ4MA+4uIPJ4x6GlgU9ufU0r3Byb0OqXkSQtN+Cx4H7UH/OnAd5pdTgGrKhL9sTOB5ymlF2aX2U7d7qqKjWPf/DCHLxvjYucPRIR/d7dDwDa5321i9UffIgmDPGx7qgo4WvODQ8W434sIi7mr7QY2WwW2dkj/Im0RebJrBkFnMxnG/Nrpyvd22fYuYIP9swgxeQ7YFR8/LNFokVQVNQe8tvUnIvIgej8/Hwa2lf6rgl0i1dbkbQ6Eq6+qPr+KCGYUtiFgs1kkW6oxsPeOOo9wZp0Oqoqka9vGkYXmNAr8R+WgPhhsXgcHGnP6JhJACKyqqApxtmx3o4HPSHD0XVXFS5fOjNDH3Jq+pAtsqvx3Zbc/icij0Umt7GfzIx6XMbtrzxFwbSvPRQRveaqZx2WSjNdNSKIPWeTAmeaGdG+3pNwENo+IdHPDbu9MmCDJBHGc9kZEbkdQ0XNVReMeFv2eioib6vaAa+kOu/7eBFWVsMKW8X0TkdCPDACTlqIpZYxGyhvtcT/WkO6tGYlF7WhmALMgjnN9LCKbPL8FXKod402Rrk3swrNOBEbK7wptcM2lBXyhduYETjmXPJFVErbFDOfdAtZipV6LyNHKxcb8FgMTQUiSctuE0A2whYzypWnqvFKlbexarV+JyN1y1T3gOrMiXdu972x51pUSNmgSkavNRe0jPOA6pn0xwztfhw0b8EU4HQFe4kWvEbiroZ6ES+C3IkJtOWyqSsy7Sig6L+AAc42abiPmQoQgroZ1LCceX5ikB0wsyxOiJlwXzj3PC0SZz4YLdKDDUB5vtTD27rld7JM94DIkjQLX4eAAT/jKUHh0gC+ijAfMbiPnpBu33vG+OAvAo/pySOZ0oJ5NzSxU/yMqfaOdFov9UYclq4BcObtPMfHoaqgHvGyntDq1tPFLp7sJqx4wcbesdAx56lFPtDK1dPYBm8pHa7dEoC8LY9PseDFwXaXh/Ikt41VrAdf59LRK5WLgMmmiBrep0rSA68xpSrFtpQ2rau173EJer4hXF7mHjjIiW14lYVXF75R5v7ut7QGTQ5c5aVjVj2BNwmwyOEinDW9OemM72VXT0UaF+IvNtO1Yeif+IbOdFqB+mA1HnWG6GMAi1fpUs1m0iIBrKfPtqRWQcIWCDqoKbFlz6+6qwiK4U9UfOqU7CzLyvqpyglGeMISnIyPA7I1Ru/IQGlVH0stO/CPgxqlm6FhDYHM0qAzQ5dYPaAL7lHp1BFg+b9weap4nhYmH93EnbaPbtaq3OTw8fH1QNlQNYcJDEs4L4AT3/Gj3bZo9Ei20zLs9RHGAqxdD5rUL2D7M6pJ61pUNVJwU9FSYqRfCpMpRqHdphYtv90dhd0u4kLRn0/kxwNSRToEXoMT9ssqZv+OeDkaas1vCBTSTYCfiXRijG87s/Y3Y0evAdkzLeNTGWjcNCD1I9WIXFIHm54eBC3Amhoq37kaWksfO6toyC4fGkDFFNfDTF+BOA5tdM2lUj9+KqiW2+uismRy24Zb6mN0hcRxbS9VHtY9LqqgtoNNi/RQJN+I26pmvA6Oy9XXB+jUAAcPZvZghTW9ey4A7i7Cx01VwHxx4VJdX9rtWCa8EGR37xgH/B89xhFvgqzNaAAAAAElFTkSuQmCC');
}
.search {
    padding: 0.5rem;
}
.search-box {
    background: #fff;
    border-radius: 3px;
    position: relative;
}
.search-box input {
    text-align: center;
    width: 100%;
    font-size: 0.8rem;
    padding: 0.4rem 0;
    border: 1px solid #E8E8E8;
}
.icon-search {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAFJElEQVRoQ+2aTVYbORCAS213b8OcIHCCkBMEThDmBDOcIPEC6bEKWfEkL4ATjOcEIScYOEGcE0xygiFbA13zyk/t15ZLLclu446DVjwQUn+qH1WVSsAvNsQvxgvPwNsu8bVI+Pz8fDfLsjdCiAMA2AWAfQDYYQ7zBhHvhBA3AHArpRyv+8BbAybIXq/3FhHfCyEIMnkg4jcAuC7L8ur09JR+bn2sDGxBPwDAny1/3Y0Q4uPJyQlJv7WxNPDFxcXOw8PDO0Q8i/ia7wAwJzFE3BFCvIr431Ge54PBYHAXMTc4ZSlgY8w+In7yqS4ifiXVFEJch+zSrnVg7f2t54vvEPFYKXUdJApMSAY2xpDq/sWti4h/l2V5tqz9WWdH65MfeOHugYiXSqnBKtBJwMPh8AOnwquCugBkLpPJhKDJN7hjJKU8XhY6GtgYcwkA7+obIeKPLMuO2nYs1R5W3UeMrS8NHQXMqTHZaVEUB205E5/ErLQvhRB/OHOWgg4CD4fDA0T8x5Hsk8DW99Rak6Rd6GMp5ShFvRuB6XTv7+//rUdJTyVZDoKBpqvqMHQT1NdqBGY2+J7n+f661bhJYsYYCkTe1ObcSCkPY6XsBeZUGQBep5xm7EekzLM2/c25tqJV2wtsjCG7peC/GldSyvcpH7euua4TpRhcKbUXsx8L7EqXrp+iKHY3qcouDKPaUVJmgV3bRcSPSqmYmDnmkFuZw5jcWEr5OrQ4C2yM+a/yzF2UbgWltR7Xg5LHx8e9UFi7AKy1PhJCfKoWpbBRKdV26hcSRNTftdYUfl7UvjWoiQvAbgiJiL+3kaVEESROsrk4xQnVoKpJ3dEurMgBz91zeZ7/1iVnxTgvyrNfVr+XUjbGFhww1lTkq1KK6lGdHcYYypFneXTIjueAGRX5LKU86iwtAGitz+pppBDisCl7mwNm7t+gE9j0YTCZXON9/NMDpwrpGbie+3YxwnJNiLmLG6/RRgkDQGcSBp+vWMlp0aLGmNm1ZJ8/Gi/yDjituVpbkpemj9da01vPtESaknZtCtzNmkKBEhd4JF3kmwKlfW0JihKd6aDyUyhQ4pIHNyAfKKVIbTo33EQnxudwEqZQ8kuNLirP3MRpMHl7MNHx5cNzAXkoPt0ELFdRDdkvfaev4uGqdedyYvc6is3bWWBPZXDjFctKkzjpxmqhN3d0TxAAkuq/61RzrTU91c6yuFjpelW6cvmTyWSu/tuFUJN754qVbiOwjboW3oJDkcw6JUuviQBA9fJZg0yqEIKPaW5FAQCS33PaOATrV744XQfBGpa7dxDYOghqJ5rVjTYB7WZFBJKiyhV4ENiqNvV0UFeN24YQVe1vQ8IcMAAk7x8F3ASNiNdFURw/RWWTMS/6tCToaOCApCnDuuz3+1frBLd2TJrmtjtFQycBE7TttKGWJK7HitqLRst00jGdfGxLgw869sEgGbiyRyYwmTNVyqVtDyU5vGkPpZTyttIUAHiBiNM+TNujtVD/9l2BHuio22Np4EravV6PeizqL/Jt+KjpGk1e2BP+BqFXAq7IbKmUHst9nXSph3ArhDgLtUPZtib39miEbgW4orH2Ta+PFOcmSb1qVyzLchR68qyfng86z/M9zoG2CuyK0Up+19oqWFulaWPqk6YAJsuycb/fH6/i3T3Q4zzPD9111wqcqserzPc04SxUa7YGODbZ2SpgF5raNcqy3K/7hK0DJmhS77IsqQd7oV97K4GbfMEz8Cqe8mf43/8BI1hVaoEimFMAAAAASUVORK5CYII=');
    position: absolute;
    width: 16px;
    height: 16px;
    margin-left: -35px;
    left: 50%;
    top: 0.4rem;
    background-size: 16px;
}
.palace-one {
    background: #fff;
    padding: 0.5rem 1rem;
}
.palace-one .palace-grid {
    width: 25%;
}
.palace-one h2 {
    font-size: 0.7rem;
}
.palace-one .palace-grid-icon {
    width: 35px;
    height: 35px;
}
.flex-clear {
    background: #fff;
}
.flex-clear h3 {
    font-weight: normal;
    font-size: 0.9rem;
}
.flex-clear span {
    color: #868686;
    font-size: 0.8rem;
}
.img-sml {
    width: 35px;
    height: 35px;
    margin-right: 0.5rem;
}
.me-list {
    background: #fff;
}
.img-sml img {
    border-radius: 100%;
}
.flex-box span {
    color: #777777;
    font-size: 0.75rem;
}
.text {
    font-size: 0.7rem;
    color: #afafaf;
}
.footer {
    width: 100%;
    position: relative;
    z-index: 100;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    padding: 7px 5px 7px 5px;
    background: #fafafa;
}
.footer:after {
    content: '';
    position: absolute;
    z-index: 0;
    top: -1px;
    left: 0;
    width: 100%;
    height: 1px;
    border-bottom: 1px solid #D9D9D9;
    -webkit-transform: scaleY(0.5);
    transform: scaleY(0.5);
    -webkit-transform-origin: 0 100%;
    transform-origin: 0 100%;
}
.tabBar-item {
    -webkit-box-flex: 1;
    -webkit-flex: 1;
    -ms-flex: 1;
    flex: 1;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -webkit-flex-direction: column;
    -ms-flex-direction: column;
    flex-direction: column;
    -webkit-box-pack: center;
    -webkit-justify-content: center;
    -ms-flex-pack: center;
    justify-content: center;
    -webkit-box-align: center;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    color: #979797;
}
.tabBar-item-text {
    display: inline-block;
    font-size: 0.6rem;
    color: #999;
    padding-top: 2px;
}
.tabBar-item-active .tabBar-item-text {
    color: #00a9ea;
}
.icon-loan {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAD1ElEQVRoQ+1aTVbbMBDWBJttuUHhBG1PUHqCwgmanACykHisGlY8pAVwAugJgBM0nID0BNATFLbYePo+np2nxP/5cWywduFJeL75ZqSZTyLxzga9M7yiBfzWGW8Zbhl+Yx7IDWljzHchxOeG4B5JKW+ybE0FbIz5KYTYF0JsNARsZOajEOJMSnmUZHciYK31BRF1GwZ0wlxmvlRK9aYxxABrrbtEdNFksJHtzNxTSl3aWJIA3xPRpjXprxACi4Y1d8K2EAJR+dECPFJKfUkFfHx8vOk4zr214Ml13c1+v4+8qP04PT3d8DzvgYg+RMZKKSdInfhhjIGXfluAb5VS+FtjhtZ6SERfLYO/SSnH0dkCnmI4lgN1p1prfUdEdt1QnOEQ3ND3/d7h4eFDncFi/1lbW7uaAguTSwPGokdmHiilzusIWmu9R0SDlCJpJsARzlqxHZ4qqBmyNta5AL+yHQRB7+Dg4HqVbOewaptWCjCKDozxYW4dWdeu6/aqPqNx1vq+f5XCapK9xQEz863rujue5w2IaC+B0UrZPjk52el0OgjhWEPDzOeu6w48z7teyDmMooSZ8c/GVUxVbIcVFBqanQSng9VuVFwstPAIwwl1NXrk6YHyc9euahaR40VYtdNqoYAjADCCiC6T2EYv6jjO0by5ncUqMz8xczdp41wKYADPYpuZUcD3ZmU7TB+EsN21Rf6+cRynm+bQpQFeBtuhEyOlZSIjsli1Jy4dMD4WlnUIcbtLebUDbCO3lVKjrJyeh9XKAUcfNMbsowRNye1Bks6Uxyp0tWnVIstxlTBsG5DDNliG7PLKttYaXQ1yNaaKogZ4eXnplm1aKgdclO1wHgr+WK6iEZBSns1yrK0McMQgji8hxKcixs/K6spyOA2UMQZMYvfNGv1ZWa0d4By2/6CIyNvFi0RI+J16aVpTbB9JKWN5XBRc0ryV5vA8hs+6tgVcRtPCrtnq0rPGWkXr2pBuQ9oKtfZuqd20Ktp55vhMu2llbVroT4noLnIw1Aql1NYcDq98qTHmn61b+76/ZffUSU8eHm3FIgiC3VVfqxT12vT7FOhgSqkJ0T4G2BiD/vWH9ZGl6M1FQRSdl6Rf4zZCKYWnV+MRAxxKNKNpXSq8dcgU4ooat+h5zIxUnLiVALtJ71MS32mF3sKFVZPHxCVaBCT1JR7yAbcIKQpkbR2Rp19nvrUML5zRoNs5XVuwQohfvu8PspTO3MelQAft+Pn5ebvT6dTykWkQBKP19fVhkfusQoDrTGlZ21rAZT3WtPktw01jrKy9LcNlPda0+f8BqLojal4/ZaEAAAAASUVORK5CYII=');
}
.icon-credit {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAGWUlEQVRoQ+Wbf07cOBTH7ZlE4r/tnmDhBAsnKD1B2RMUTlCQsBF/LfsXwkGie4LCCQon6OwJCiconGBn/4XMvNU3crKOYydxxhm0aiRUqSS2P34//N7zg7Mf7OE/GC9bK7BS6q1rg6WUf61r40cDBhznfJcxhp9txtibDqg5Y+yeMTYjotlYmxAVOMuy90S0xznfjyExIrrmnN8KIe5ijIcxVga+urp68/Ly8oExdsg534y1MHMcInqcTCZn0+n07ujoCJow+FkJ+PLy8gMRfeqhrtUCiegfrbr4v23O+U8Bq59zzg+Pj49vAr6pvToIWCmFhV5p+3TODTDO+Qw2CcAkSe590oGW5HkOO8fPLhHtdmwE7PxISgmbD3qCgZVSHznnZy1SvVsul9cnJye3QSuxXr64uNibTCbwBe8948w19HXIPEHASqnPLQ7pJs/zs9PT08eQBXS9e35+vpkkCTYYfqLxwLFJKQ+6xil/3wtYq9wXlwoTEc7QwyHq1XeReA9mxBj7xDlvnOVEdJum6UEfh9YJrL3wV845JrSfIyEEnNbanizLIO3f7QmJ6F5KudO1kE5glxprT7s7tlR9i9fSntmOrY96twIrpaBCH62JH4ho/7Vgy7XokwIO61dzfUT0p5Ty0LdZXmDtJWG31QPJpmm62cdWulQrxu/h0KbT6b0t6eVy+ZvvlHACayf13Tx6XluNA9V7niTJlkswTmCl1BfO+Z45SduuxZDWKmO4tJExdiOEaMT0DeAsy5DdfA2xiyGLhQ2mafoYyzw8/uadEAKRXvW4gAEL6PJ5SpJkO9bCMKhS6ruRaDQWNWQDtRki1PzF+H4mhHjnBfZI90BKGRS+tS3YMYdT9YZAK6X2OeefrW9rG1qTcJZlADNDuCchRNSUzwZGpCalNDVqCGv1TZZlCG1NKdc2tALWKvG3ZbtRpYuxxwZ2SLnmsStg+0UcQ1LKrrJMsDTGBtY+AnlzlWcTUSW4CtihztFsy9yVdQC3sZjAUOdKomOdu+sAts9llIiklFvY+AJY55yIrKonSZKfYx5F5cDrAHb5ozzPt5CrF8COo+JBCOFKB4Nt1v5gHcCayfbWxfFUAtdyzNhHxbptWDsupI9msaDI3Z3AjLE/hBDYhKDHd7NgDYICYFU0QOKOiknXRGmaPoSYmKNQUDBFA7bCxa71D/o9Ee30zcNbgR2Bd5CEdTL+bRBF2Ee912UDl4WBKBJ2ecUwjn5vmwFE1xdBKt1VJnFNpr3vPhG1xt6cc5z1VVnGuonwcuCOKUmS6752HAocNaB/DS+dZRkuAswi/n9OyxGZ/O+BlVK1Y6mMHAsbdjkdIURnCbfLjlpUv6qojHXmZ1lG5vylhzezpVqGwRiLUol4jUjLVcgoBWgmD06dHyLFtm/WEVo6jqTKRE1gRDu4Ai0eM8OICb0OYEcQVF0JVcCujGkMtR4b2OWPykwJgrNrWrZa3wkhavXpVaU9NrAj+a9lfjVgV0Hb3J1VYfH9mMAuLbWjM1dd2s4jG7XdVcAdYWi0K9csyxo1dbvq2gD21HajLco49/fgGNM0ve0bLrZttOfyr1F19d0t2cnzPM/zndjtDKtoivmtVmVka2aV1Vm18QEjSbfTvegOLBawUuqbo0PBGTh5w0d7kCEZVCygtnE8HQreS3EnsMfb9a42rANU+wJXV1FrAdKn0narw2hVzCGboxttAFuLEZBbLxaL7TZf4wM2rzOxpqheeghk+Y1uaAFsrYzct0PBdSw1HFbs4GMosK8LsC9sI7TUkVDtyrRPvqp3nfWtKIYCIzojoitPr9gTWpb7zu2KtGp3THZoph0aalJl43d1t4tAAt1yi8XiLsaZrbt10afhvD+GMNI03QsJXOzkodHfwRiDYyi6XHt2tpcCRPByHdLjrMPOt7rJHPO2Xdf2LtmaGmUDO9v6QlXQ9T5uGDjn6IB95JybDaiA2ka1s0+DOaS6WCz2h2qQDVwrAsQAjTUGQNGMvmpbcg1Yn2+QQFeX+oPuase90D1u5cq6tK/NdwVwdL9f2+1HQ8fzHUsoBJSNIU8G3Kytsx2LwKY9Pz/vTiYT2CDs3mww6bNOzFf8ZUusTMprw3YGsrGxMQ/xgC4aq72/cEJEVPwLm9bfFH/C07WZfXar651Ras9dk77m7/8FVgstedz4YZ4AAAAASUVORK5CYII=');
}
.icon-ions {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAFa0lEQVRoQ+1b23ETSRTtlkffCxEAESwbwdoRABEgIkCqcrfLX8hfLs+4SnYEiAjWRICIYHEEyBmYb2vmbh1Xj6rd6te8veudHyg0j3v6vs59wNkTu/gQeE9PT1/iu8fHx+u+v98b4MVi8Wyz2XxkjE0ZY88U0FvG2EWSJJez2Qx/7/zqBfD5+fl7IrrQgJrAbjnn08PDwy9dI+4UcJZl+0S04Jy/jgSyYoydCCHwZydXJ4Bhvnd3dwA6sUlNRN855zDr3x2/L8fj8awLM28dcJZlnww/1TFd47dSg7AA+LAD+C0RzaWUl22qujXAynw/c87vI7B+EdEvAJVSLm3Cp2kKS7jgnP9meXbNOf/Qlpk3BowUkyTJZ8YYtLVzEdHleDyeh8xTucGcc45IbnvPVZ7ns6aprDZgLc3MXX6a5/mkqoBpmiLAQdt/Okx53iSN1QKMNFMUBbSxY76MsZuiKKZHR0dXTXzv7Ozs7Wg0gn+/sJn5aDSa10ljlQDj9DnnC5v5wk855yARFyHzjT0IZUVTIpra/JsxtiKimZTyR+w7owCH0gxj7Otms5lWNd9YIVWcgLbfOJ7BQZ/EHHQQMCKo0mpJB51pJhZA3fsi0hi0bc0E5Te9gNM0/QgztaUZzvlcCLHzW10wVZ7LsgxmjhhiS2MffKCdgNM0RaTcSRGxaaYKgDr3Kv/Ggb+3KORSSokiZefyAf6pR2HQQUUeogNEHSBVn7GlMSJaSylfRQNWQeKn9sBXIcTbqsL0eX+WZUiD26C22Wxe2YKoVcMqUIE9lRcqGCvBqAoKh7m3t3efW/M8v2krsltkPrDRUSvgLMsADkVAK4AVV37DOQf9NKM9ioTVaDS6qkMkSgFVBP+mydw/YB9RcVhGZSLxaAAH8rfPE6DxYD41XzCohi3+tJVPRfsy0oOqWosEIvLm00cDWJkxfMn0VWfgs8QM4IGmD2J58mAaTtN0ZWjtmogmIcHVQYEW6m2flRDiICYTDALYZspE9EcIbAlIgf5bB1gUxbuYUnMQwGbyVx3ISvnbYt5RpGcQwGmaor+8JfRCiGA1ZjPXLMtI+/dbIcTzkFn3Dtiko4jGUkprnyskvBkHkiR5Hqp1ewdsfhBVlatiiQBsVmpW1qS/53/AjHVLLZ+cScO8ughaaA5KKW3tpQee0btJ4+sdpaUvQgjrjGpQH1YaRsNPr6PZf5p4KNAPqCURoVBAIeBtDalWDWZT29FqldQ2iEkrwBAYoM2OIrqcJw6iYTYcYBkYwO2HDupR1MO+8hCHwRjbloeeIdy/ozzUCgHnCNRHPEKjVdezg5m0LlDEJPCB/E1awY8CcIlGTQInRLRv+rYawq2KoljGlIFdaRhde0wJy6u1Nq2aGNxH4iRJfoSKghDvNg71L+3+StQSVc625dmkEIgVuOl95mjIlf+t9apl8gB5nGmlqbBNn1eLNNtGg4+OOgt0C01EblyjhdrE15qC059HbMAo17KJ4OySOAErX0O+3Fk5qDN5bxNooMF/nSTJvis2eFswavJ/5ekdd7ZAZjugmE2EJEkmvkAY1XPyLZigf4ytGxdtbEuzgYW36EWaKMAaX527Fky68m+Pn97z7aqbCJUAA3hogUxx5cYLooo5YYLZaOHNtLDKgMsXqDnv0uffeZ6fVJ3/qvd+8i2m1ll4K+WuDdgoyzAisUXz6AVwxwK5rqAbxtik6c5lY8AacN9mzdq3Oefb7Kvjp75A2RrgOv7dlZ/2BjjWv1Vgw+2ugPS9iZ/2DjjSv21yPVggbyuH6+9p1aRdAvoWwPFM3S5HnQPpBXDp31hANYgLIu+yzQ3c0CH0BlgX5En8R63Qyff1+z/dmjB5kg07lwAAAABJRU5ErkJggg==');
}
.icon-info {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAADqUlEQVRoQ+2a/XXaQAzAJZPXj+cP6ARNJmg2aDpB8AQJEyRM0GSC0AlCJjiYIGzQdIImGwQ4Xps+sPqOxA0PMNzZusN94H+RdfqdhKTTGWHLHtwyXtgB2/K4L+ThBCqPv+P397bW0NFrx8OCaqE3OvaI6gBYX24IdRLEzjDxuxDjo46xHDK8wIJqEY6uEODUxDhCaA0S/9IFOBtw1JVnSHQBgDUT2FdZekwIm8M4aOd7X+8tFuCoI69NvZpl3tTbx0FTz3xzqcLAnLCp+QTQHtSDhjnO+jcKAUdCthDhbP0y5hJEdDmIwwvzN1e/kRs4FKO6hyS4DZrVNyH6IuOwx7lGPmBBtSrKn/kTlDbCfb8eHGhLawjmAo7E8AIRv2roLyySEDQ4M7c5sDvvppvF6mVjYBf/3fmwSAjjYex3CocLgPnhIRKyjQgnHIvr6iCCb4M4ONeVXyVn7OFqRyUr2OdY3EAHW1jnASYDQ9lE+/XA2NZlixspCcTwqIJ4y0ZhoKhP/geOw8V/A8zVhOyAV0XZJkP6iSoHHNMSIw+rMc0ewneDvx6b6EaSlrK+2pHbk6WnwELeAcInNtdpKCKi7iAOM2ZjGgpmRIxCWr0XCXmOCFdmyxST5jxAGAO/E7/23+JEdVtuHqJ+Pw5zzskWTTQGfvGys36aCG4GcWA0BWXtpZWyqZdhfAeIVatuVt6FYJ+jw0rtzOXhZy/bHwIQQXMQBy3OTc0NbDtjc2bm2Q0rBAxq+gGjHnuZIvjRB/+IM5QLh/S/XeOGJnjog39oA1bZXMzDABB25YlH1GKeYPaeqNLg6J3n//+5gV/q8TUAHHEmlVdd6q7Ja6hZllprrwIf59cZT+DBdFNyAT8fIuiW2asL+5bePmRVhDy3E8bAoZCnHoLyrPVn48CuR7QbBXYVxrNhszlg97cNU+6NAVsbvhM8AFDmRy4JYFvdKzlNWjbnWLpZ1imwzZuGFFjV2Tdeknl9g0Sq1i+r9z1CzLw//pN4N/N1emVZsl2CUmBbUbRslr0S2KZ3Z5NSKYBdjGRL5WGbH6yktbZUwLbDuVQh7SKcZ4HVICEAeZjVnHuAp8su4dWALwHK/HJPQnA3f65emrRczZ5LU4etdVaLLlRdVnanRXDjpNOqimEPED9bP/+tWcBZL72pC7N5/h3w3I7o5oC1Y9qt8rCrkqSTH9yE9JqaqGMol8wY9u7VaWc6tYTxwrdh6e8m6xkP8UyUl1F2B1xGr3Da9BfBoGNbQjaXpAAAAABJRU5ErkJggg==');
}
.icon-mine {
    background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAE7klEQVRoQ+2aQVYbORCGVW17Pc4JJpxgyAkGThDnBAMnCH4PicdqmBUPaQGcIMMJAieI5wQxJwhzgvGsEV15laf2qGXJtKWyh0B6CZKsr/+qUqmqQbywB14Yr/gBvA7FtdbbAPBWCLFD6yPiEABm7remADDt9Xo34/G4+ds6tvFtzbUpfH5+PrTWvkfEPQB43YUAEa8B4FJKOekyPmfMWoCNMb8LIQ6EEMOcTQkhJtba/ePj47vM+clprMBO1Y+N6RZudlbX9f7R0dF14Tqt6WzAp6enr3u93kcA2I5tEBH/BQDafKjaSAjxSwoKEfeVUn9yQbMAk7L39/efYrCI+BciXixTil5Wv9/fQ8QDAPgphOOEZgHWWpOypNT8IUXJj1dRx4GTFYSKzxBxVyk1LVW6GFhrTVH4QwR2J3eDxhgy4d8CuImUcvcpAH8Jjx1EfJML2wBprScA8GvwIov9uUjhmLpCiLGU8qJUCRcX7nyfRsQ7pdRWydpFwMYY8jfKoJrnbyllpySjy6aNMXSWnwcqF1lPNrA7c/8JNs6irr+m1noWRO4/pJQnXV5YbEw2sDGG8uJP/qLW2i3u7CgMYHTMKaW+5eQ5TwkwvWVKIZvnVkoZTTpyNtbMiZj1TEr5KndNNuDSN58CiFmSlDJ739kTjTEthX8A59pcMO8pKzxVSr1h4pwvE/HhoqOvxKQ3FaVbZ32p62QDb+ocNsbQWe8XEorO+mxgsrkw0+JI/XyXCAMj/a80Ty8CTuTSRZlQA+ws6EugbpH/0tpFwE5lqmD8zJnvunUpi2tlVHVdvyst+RQDn52djaqqojqW/xRd2LXWHwBgL3iJRSlls1YxsFMjdmEn6BOl1GXXoypVF3PVk+yCgv/7LMDO36iWHCvG0d8vpJQ3KXBX2qEKR/QWxGHKrArTYo9A0xBSnKoYfl1qiIg7qUqni8rFVQ52hYPISubtFwW6WnRrnCvrjri7ECwmHRJROkj+Gyu5dqS/sdYecN+tWY6lFIAzcSrRULRtHVtLoMnPyd+/r95SCOS6h1S33qbOYcunACaUoQ0Gg+vvunvY0XQ3PozVh0lJIcRCq6SUajAY3HKpnw1MPvrw8PC2rutR2GYpBUzNJ9OnhhwiXuUW+lcGdkkCtVayK4ccL4Tgq6o6OTw8vFplvc7ATUc/lQ2t8qPMYynojbsq3gl4WTuUefPZy3VtqT4K/FijWwhxK4Sg7Gpqrb3jThacZW3XdT2sqmqEiBQzooGxC/RS4MQlvFHhylp7wg3YRWIqPFCCktM8XwpsjFm4hK8rx+0C6o9xYsTy9qV38SRwonNHXX2We+mqgKnxseY5IiZLxlFgd/R89utJnJdwLthmncQXA9HaWhRYa03+8d7fGOclnBvYmTfds/1Lyqzf72+FGdoCcCJQ3UgpWx+tcG+6dL1YSyYWtReAY7XgdfR9SwFj88PvQmJ18gVgrfVnv+RS2tpYB1hqzcQXRa1PJFrALlhR8Xv+PGXfjYEbY8I6eSt4tYBjR1FJ83mT6qYidnhEhcCsnbr/AzjWGPBjUAtYax1+ZMbSJ9okeKKrudvUyUKF0d8cfexJl4JNbpjjt9xXu9EW6xzYFdoou3p2DyJeKqVIvP+6h7GD+7mQ+0fri1BYCDHPFMOgtZBDPwOVb621o+be/mjF4xkAtxBeHPBXecb3W6KsxwkAAAAASUVORK5CYII=');
}
.footer-fixed {
    position: fixed;
    bottom: 0;
    left: 0;
    z-index: 49;
}


</style>
<template>
    <div class="cover">
        <div class="cover-left" v-for="item of coverlist" :key="item.id" v-if="item.id == 1">
            <div class="left-info">
                <span class="left-info-title">{{item.title}}</span>
                <span class="left-info-desc">{{item.desc}}</span>
            </div>
            <img class="cover-left-img" :src="item.imgUrl">
        </div>
        <div class="cover-right">
            <div class="right-top" v-for="item of coverlist" :key="item.id" v-if="item.id == 2">
                <div class="right-info">
                    <span class="right-info-title">{{item.title}}</span>
                    <span class="right-info-desc">{{item.desc}}</span>
                </div>
                <img class="cover-right-img" :src="item.imgUrl">
            </div>
            <div class="right-bottom" v-for="item of coverlist" :key="item.id" v-if="item.id == 3">
                <div class="right-info">
                    <span class="right-info-title">{{item.title}}</span>
                    <span class="right-info-desc">{{item.desc}}</span>
                </div>
                <img class="cover-right-img" :src="item.imgUrl">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Cover',
    props: {
        coverlist: Array
    }  
}
</script>

<style lang="stylus" scoped>
    .cover
        border-top .5rem solid #eee
        overflow hidden
        height 0
        padding-bottom 73%
        .cover-left
            width 50%
            box-sizing border-box
            padding-left .9rem
            padding-right .9rem
            padding-bottom 73%
            float left 
            .left-info
                width 100%
                height 2rem
                .left-info-title
                    display block
                    height 1.5rem
                    line-height 1.5rem
                    font-size .6rem
                    font-weight bold
                .left-info-desc
                    display block
                    font-size .5rem
                    color #777
            .cover-left-img
                margin-top .5rem
                width 100%

        .cover-right
            width 50%
            float left
            padding-bottom 73%
            .right-top
                width 100%
                padding-bottom 73%
                height 0
                overflow hidden
                .right-info
                    width 100%
                    height 2rem
                    .right-info-title
                        display block
                        height 1.5rem
                        line-height 1.5rem
                        font-size .6rem
                        font-weight bold
                    .right-info-desc
                        display block
                        font-size .5rem
                        color #777
                .cover-right-img
                    margin-top .2rem
                    width 100%
            .right-bottom
                .right-info
                    width 100%
                    height 2rem
                    .right-info-title
                        display block
                        height 1.5rem
                        line-height 1.5rem
                        font-size .6rem
                        font-weight bold
                    .right-info-desc
                        display block
                        font-size .5rem
                        color #777
                .cover-right-img
                    margin-top .2rem
                    width 100%

</style>

<template>
    <div class="f-flex m-header">
        <div class="f-flex f-flextc f-flexvc back" @click="goBack">返回</div>
        <div class="f-flex1 back"></div>
        <div class="tab"></div>
    </div>
</template>
<script>
import { mapActions } from 'vuex'
export default {
    name: 'header',
    data() {
        return {

        }
    },
    methods: {
        ...mapActions([
            'setDirection'
        ]),
        goBack() {
            this.setDirection('reverse');
            this.$router.go(-1);
        }
    },
    created: function() {

    },
    mounted: function() {

    }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
.m-header {
    height: 40px;
    background: #385FB5;
    color: #fff;
    .back,
    .tab {
        width: 60px;
        font-size: 14px;
    }
}
</style>

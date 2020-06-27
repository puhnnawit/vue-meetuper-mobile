<template>
    <view>
        <text class="text-color-primary">{{message}}</text>
        <text class="text-click-count">{{clickCount}}</text>
        <text>{{clickMotivation}}</text>
        <Button :title="btnMessage"
                :on-press="handleClick" />
        <touchable-opacity>
            <Text>{{btnMessage}}</Text>
        </touchable-opacity>
    </view>
</template>

<script>
export default {
    data() {
        return {
            message : 'Welcome to my application',
            btnMessage : 'Click Me',
            clickCount: 0
        }
    },
    computed: {
        clickMotivation() {
            if (this.clickCount < 5) {
                return "Please click me"
            }else {
                return "Good job! Keep clicking"
            }
        }
    },
    methods: {
        handleClick() {
            this.clickCount++
        }
    }
}
</script>

<style>
.text-color-primary {
  color: blue;
}
.text-click-count {
  font-size: 30px;
}

</style>
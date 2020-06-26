<template>
    <view>
        <text class="text-color-primary">{{message}}</text>
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
    methods: {
        handleClick() {
            this.clickCount = this.clickCount + 1
            alert(`I'm clicked, Click Count: ${this.clickCount}`)
        }
    }
}
</script>

<style>
.text-color-primary {
  color: blue;
}

</style>
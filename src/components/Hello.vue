<template>
    <view>
        <text class="text-color-primary">{{message}}</text>
        <Button :title="btnMessage" ></Button>
        <touchable-opacity ><Text>Press Here</Text></touchable-opacity>
    </view>
</template>

<script>
export default {
    data() {
        return {
            message : 'Welcome to my application',
            btnMessage : 'Click Me'
        }
    }
}
</script>

<style>
.text-color-primary {
  color: blue;
}

</style>
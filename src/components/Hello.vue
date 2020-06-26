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
            btnMessage : 'Click Me'
        }
    },
    methods: {
        handleClick() {
            alert("I'm clicked")
        }
    }
}
</script>

<style>
.text-color-primary {
  color: blue;
}

</style>
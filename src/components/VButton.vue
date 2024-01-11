<!-- Button Component with props:
        - required text
        - default height
        - default width
     Button should also:
        - emit an event when clicked
        - on click trigger a native alert message
     Extra:
        - Before and after slots
        - 'dark' prop
-->

<template>
    <v-btn class="v-button" :name="name" :width="width" :height="height" :dark="dark" :style="{
        backgroundColor: dark ? 'black' : 'white',
        color: dark ? 'white' : 'black'
    }" :rounded="rounded" :elevation=14 @click="handleClick">
        <slot name="before"></slot>
        {{ name }}
        <slot name="after">
            <font-awesome-icon icon="fa-solid fa-computer-mouse" style="margin-left: 8px;" />
        </slot>
    </v-btn>
</template>

<script>
export default {
    name: 'VButton',
    props: {
        name: {
            type: String,
            required: true
        },
        width: {
            type: Number,
            default: 250
        },
        height: {
            type: Number,
            default: 100
        },
        rounded: {
            type: Boolean,
            default: true
        },
        dark: {
            type: Boolean
        },
        ripple: {
            type: Boolean,
            default: true
        }
    },
    methods: {
        handleClick() {
            this.$emit('button-click', this.text);
        }
    }
};
</script>

<style lang="scss" scoped>
.v-button {
    padding: 10px 20px;
    text-align: center;
    text-decoration: none;
    text-transform: none;
    display: inline-block;
    font-size: 28px;
    cursor: pointer;
}
</style>

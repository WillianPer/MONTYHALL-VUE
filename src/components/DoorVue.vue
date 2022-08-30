<!-- eslint-disable vue/valid-template-root -->
// eslint-disable-next-line vue/valid-template-root
<template>
    <div class="door-area">
        <div class="door-frame">
            <Gift v-if="open && hasGift"/>
        </div>
        <div class="door">
            <div class="nunber">{{ number }}</div>
            <div class="knob"></div>
        </div>
    </div>
</template>

<script>
import Gift from './GiftVue.vue';

export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Door",
    // eslint-disable-next-line vue/no-unused-components
    components: {Gift},
    props: {
        number: {},
        hasGift: { type: Boolean}
    },
    data: function () {
        return {
            open: false,
            selected: false
        }
    }

}
</script>

<style>
    :root {
        --door-border: 5px solid brown;
    }

    .door-area {
        position: relative;
        width: 200px;
        height: 310px;
        border-bottom: 10px solid #AAA;
        margin-bottom: 20px;
        font-size: 3rem;

        display: flex;
        justify-content: center;

    }

    .door-frame {
        position: absolute;
        width: 180px;
        height: 300px;

        border-left: var(--door-border);
        border-top: var(--door-border);
        border-right: var(--door-border);

        display: flex;
        justify-content: center;
        align-items: flex-end;
    }

    .door {
        position: absolute;
        top: 5px;
        height: 295px;
        width: 170px;
        background-color: chocolate;

        display: flex;
        flex-direction: column;
        padding: 20px;
    }
</style>
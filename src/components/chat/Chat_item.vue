<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    chat: {
        type: Object,
        required: true,
    },
    messages: {
        type: Array,
        required: true,
    },
});
</script>

<template>
    <div :class="$style.user_chat">
        <div :class="$style.user_left">
            <div>
                <img :src="chat.image" alt="User Image">
            </div>
            <div>
                <div :class="$style.user_name">
                    <img :src="chat.flag" alt="User Flag">
                    <span>{{ chat.name }}</span>
                </div>
                <div :class="$style.user_message">
                    <span>{{ chat.message }}</span>
                </div>
            </div>
        </div>
        <div :class="$style.user_right">
            <img v-if="chat.needleIcon" :src="chat.needleIcon" alt="Needle Icon">
            <img v-if="chat.messageIcon" :src="chat.messageIcon" alt="Message Icon">
        </div>
    </div>
</template>

<style module>
.user_chat {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 12px 0;
    border-bottom: 1px solid #f2f3f5;
    cursor: pointer;
}

.user_left,
.user_name {
    display: flex;
    align-items: center;
    gap: 12px;
}

.user_name {
    gap: 8px;
    margin-bottom: 12px;
}

.user_message span {
    font-weight: 500;
    font-size: 14px;
    color: #476cfa;
}

.user_right {
    display: flex;
    flex-direction: column;
    gap: 6px;
}
</style>
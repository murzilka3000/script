<script setup>
import { ref } from 'vue';
import ChatItem from './Chat_item.vue';

import user1 from '@/assets/users/1.svg';
import user2 from '@/assets/users/2.svg';
import user3 from '@/assets/users/3.svg'; 
import user4 from '@/assets/users/4.svg';

import flagRu from '@/assets/flags/ru.svg';
import flagBe from '@/assets/flags/bel.svg';
import flagKz from '@/assets/flags/kz.svg';
import needleIcon from '@/assets/needle.svg'; 
import messageIcon from '@/assets/message.svg';

const chatMessages = ref({
    1: [
        { time: '13:01', text: 'Добрый день' },
        { time: '13:02', text: 'У меня есть вопрос' },
    ],
    2: [
        { time: '13:08', text: 'Добрый день. Чем могу помочь?' },
        { time: '13:24', text: 'Проблема с настройками' },
    ],
    // Добавьте другие чаты и их сообщения по мере необходимости
});

const chats = ref([
    {
        id: 1,
        name: 'Кирилл Иванов',
        message: 'Принял',
        image: user1,
        flag: flagRu,
        needleIcon: needleIcon, 
        messageIcon: messageIcon,
    },
    {
        id: 2,
        name: 'Александр Петров',
        message: 'На связи',
        image: user2,
        flag: flagKz, 
        needleIcon: null, 
        messageIcon: messageIcon,
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 3,
        name: 'Мария Смирнова',
        message: 'Вопрос по проекту',
        image: user4,
        flag: flagKz, 
        needleIcon: needleIcon, 
        messageIcon: null, 
    },
    {
        id: 4,
        name: 'Дмитрий Сидоров',
        message: 'Отправлено',
        image: user3,
        flag: flagRu,
        needleIcon: needleIcon, 
        messageIcon: messageIcon,
    },
]);
</script>

<template>
    <div :class="$style.chat">
        <div :class="$style.mob"> 
            <h4>
                Чаты
            </h4>
        </div>
        <div :class="$style.header">
            <img src="@/assets/search.svg" alt="">
            <input placeholder="Поиск" type="text">
        </div>
        <div :class="$style.chat_container">
            <ChatItem 
                v-for="chat in chats" 
                :key="chat.id" 
                :chat="chat"
                :messages="chatMessages[chat.id]"
            />
        </div>
    </div>
</template>

<style module>
.chat {
    padding: 24px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
}

.header {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 16px 10px 24px 10px;
    border-bottom: 1px solid #f2f3f5;
}

.header input {
    width: 100%;
    border: none;
    outline: none;
}

.header input::placeholder,
.header input {
    font-weight: 500;
    font-size: 14px;
    color: #a2adc4;
}

.chat_container {
    padding-top: 22px;
    max-height: 78vh;
    overflow-y: auto; 
}

.chat_container::-webkit-scrollbar {
    display: none; 
}

.mob {
    display: none;
}

@media screen and (max-width: 767px) {
    .chat {
    padding: 44px 0 0 0;
    box-shadow: none;
}

.mob {
    display: block;
}

.mob h4 {
    font-weight: 500;
font-size: 24px;
color: #00030c;
margin-bottom: 24px;
}

}
</style>
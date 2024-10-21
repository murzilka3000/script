

<template>
    <div :class="$style.chat">
        <div :class="$style.back">
            <img src="@/assets/arrow_left.svg" alt="">
            <h2 :class="$style.name">Кирилл Иванов</h2>
        </div>
        <div :class="$style.flex">
            <img src="@/assets/Avatar.svg" alt="">
            <img src="@/assets/flags/ru.svg" alt="">
            <h4>Кирилл Иванов</h4>
            <p>IP: 127.0.0.1</p>
            <p>Москва</p>
            <p>#12345</p>
            <p>#12345</p>
            <p>#12345</p>
        </div>
        <div :class="$style.new_message" v-if="isPopupVisible">
            <img @click="hidePopup" src="@/assets/img_1.svg" alt="">
            <div>
                <img src="@/assets/mes.svg" alt="">
                <p>Новое сообщение:</p>
            </div>
            <p>
                Добрый день, мне нужна помощь
            </p>
        </div>
    </div>
</template>


<script>
export default {
  data() {
    return {
      isPopupVisible: true, 
    };
  },
  methods: {
    hidePopup() {
      this.isPopupVisible = false;
    },
  },
};
</script>

<style module>


    .new_message {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.05);
    background: #476cfa;
    border-radius: 8px;
    padding: 24px;
    position: absolute;
    bottom: 0;
    right: 0;
    } 

    .new_message > :first-child {
        position: absolute;
        top: -10px;
        right: -10px;
        cursor: pointer;
    }
    
    .new_message > :nth-child(2) {
        display: flex;
        align-items: center;
        gap: 8px;
    }

    .new_message > :nth-child(2) p {
        font-weight: 500;
        font-size: 11px;
        color: #fff;
    }

    .new_message > :nth-child(3) {
        font-weight: 500;
        font-size: 16px;
        line-height: 125%;
        color: #fff;
        margin-top: 11px;
    }

   .chat {
    padding: 88px 24px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    position: relative;
   }

   .flex {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 16px;
   }

   .flex > :nth-child(3) {
        font-weight: 500;
        font-size: 16px;
        color: #00030c;
   }

   .flex p {
    font-weight: 500;
    font-size: 14px;
    color: #a2adc4;
   }

   .back {
    display: none;
   }


   @media screen and (max-width: 767px) {
    .back {
        display: flex;
        align-items: center;
        gap: 8px;
        margin-bottom: 57px;
    }

    .chat {
        padding: 18px 0px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        border-radius: 8px;
        position: relative;
        box-shadow: none;
   }

   .name {
    font-weight: 500;
        font-size: 24px;
        color: #00030c;
   }

   .new_message {
    max-width: 200px;
   }

   .new_message > :nth-child(3) {
    font-size: 12px;
   } 
   }
 
 
</style>
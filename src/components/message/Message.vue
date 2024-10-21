<template>
    <div :class="$style.cont">
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

    @media screen and (max-width: 767px) {
        .new_message {
    max-width: 180px;
   }

   .new_message > :nth-child(3) {
    font-size: 12px;
   } 
    }
</style>
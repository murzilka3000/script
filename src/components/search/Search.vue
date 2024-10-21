

<template>
    <div :class="$style.chat">
        <div :class="$style.header">
            <div>
                <img :class="$style.mob" src="@/assets/arrow_left.svg" alt="user">
                <img id="user" src="@/assets/users/1.svg" alt="">
                <h4 id="name">Кирилл Иванов</h4>
            </div>
            <div>
                <img src="@/assets/Icon.svg" alt="">
                <img src="@/assets/Icon_two.svg" alt="">
            </div>
        </div> 
        <div :class="$style.chat_two">
            <div :class="$style.message_container">
            <div>
                <div :class="$style.message">
                    <p>13:01</p>
                    <p>Добрый день</p>
                </div>
            </div>
            <div>
                <div :class="$style.message">
                    <p>13:02</p>
                    <p>У меня есть вопрос</p>
                </div>
            </div>
            <div :class="$style.right">
                <div :class="$style.message_two">
                    <p>13:08</p>
                    <p>Добрый день. Чем могу помочь?</p>
                </div>
            </div>
            <div :class="$style.right">
                <div :class="$style.message_two">
                    <p>13:08</p>
                    <p>Добрый день. Чем могу помочь?</p>
                </div>
            </div>
            </div>
            <div :class="$style.bottom">
                <div :class="$style.message_container">
                    <div :class="$style.message_container_text">
                        <p>Сегодня</p>
                    </div>
                    <div>
                        <div :class="$style.message">
                            <p>13:24</p>
                            <p>Проблема с настройками</p>
                        </div>
                    </div>
                    
                    <div>
                        <div :class="$style.message">
                            <p>13:25</p>
                            <p>Секунду</p>
                        </div>
                    </div>
                    <div :class="$style.right">
                        <div :class="$style.message_two">
                            <p>13:29</p>
                            <p>Опишите подробнее проблему</p>
                        </div>
                    </div>
                    <div>
                        <img src="@/assets/image.jpg" alt="">
                    </div>
                    <div :class="$style.popup_container" v-if="isPopupVisible">
                        <img @click="hidePopup" src="@/assets/img_1.svg" alt="">
                        <img src="@/assets/img_2.jpg" alt="">
                        <img src="@/assets/img_3.svg" alt="">
                    </div>
                </div>
               
            </div>
        </div>
        <div :class="$style.bottom_container">
            <div>
                <img 
                src="@/assets/icon_three.svg" 
                alt="icon" 
                />
                <input placeholder="Введите сообщение" type="text">
            </div>
            <div>
                <img src="@/assets/icon_four.svg" alt="">
            </div>
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

    .popup_container {
        display: flex;
        flex-direction: column;
        max-width: 100px;
        position: fixed;
        bottom: 150px;
    }

    .popup_container > :first-child {
        position: absolute;
        right: -10px;
        top: -10px;
        cursor: pointer;
    }

    .popup_container > :nth-child(2) {
        margin-bottom: 3px;
    }


    .mob {
        display: none;
    }

    .popup-container {
    position: absolute;
    top: -50px; /* Отступ сверху от иконки */
    left: 0;
    background-color: white;
    border: 1px solid #ddd;
    padding: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    z-index: 1000;
    }


   .chat {
    padding: 24px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    position: relative;
   }

   img {
    cursor: pointer;
   }

   .header {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid #f2f3f5;
    padding-bottom: 12px;
    align-items: center;
   }

   .header > :first-child {
    display: flex;
    align-items: center;
    gap: 16px;
   }

   .header > :last-child {
    display: flex;
    align-items: center;
    gap: 21px;
   }

   .message, .message_two {
    border-radius: 4px 8px 8px 8px;
    padding: 16px;
    display: inline-block;
    background: #f2f3f5;
    margin-bottom: 8px;
   }

   .message_two {
    background: #476cfa;
    align-items: flex-end;
    display: flex;
    flex-direction: column;
   }

   .message_two > :first-child {
    font-weight: 500;
    font-size: 11px;
    color: #f2f3f5;
    margin-bottom: 8px;
   }

   .message_two > :last-child {
    font-weight: 500;
    font-size: 16px;
    color: #fff;
   }

   .message_container {
    padding-top: 40px;
    display: flex;
    flex-direction: column;
    padding-bottom: 24px;
    border-bottom: 1px solid #f2f3f5;
   }

   .bottom {
    position: relative;
   }

   .right {
    display: flex;
    justify-content: flex-end;
   }

   .message > :first-child {
    font-weight: 500;
    font-size: 11px;
    color: #a2adc4;
    margin-bottom: 8px;
   }

   .message > :last-child {
    font-weight: 500;
    font-size: 16px;
    color: #00030c;
   }

   .bottom .message_container {
    padding-top: 24px;
    border: none;
   
   }

   .message_container_text {
    display: flex!important;
    justify-content: center;
    margin-bottom: 16px;
   }

   .message_container_text p {
    font-weight: 500;
    font-size: 14px;
    text-align: center;
    color: #a2adc4;
   }

   .bottom_container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 1px solid #f2f3f5;
    position: absolute;
    bottom: 0;
    right: 0;
    left: 0;
    padding: 15px 24px;
    background-color: #fff;
   }

   .bottom_container > :first-child {
    display: flex;
    align-items: center;
    gap: 16px;
    flex: 1;
    gap: 10px;
   }

   .bottom_container > :first-child input {
    border: none;
    outline: none;
    width: 98%;
    padding: 24px 0;
   }

   .bottom_container > :first-child input, .bottom_container > :first-child input::placeholder{
    font-weight: 500;
    font-size: 16px;
    color: #a2adc4;
   }

   .chat_two {
    overflow-y: auto; 
    height: 72vh;
    }


    .chat_two::-webkit-scrollbar {
        display: none; 
    }

@media screen and (max-width: 767px) {
    .chat {
    padding: 0px;
    box-shadow: none;
    border-radius: 8px;
   }

   .bottom_container {
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
    padding: 18px;
    z-index: 999;
    background-color: #fff;
   }

   .popup_container {
        bottom: 100px;
    }

   .chat_two {
    max-height: 100vh!important;
    padding: 60px 0 90px 0;

   }

   .mob {
        display: block;
    }

    .header {
        position: fixed;
        background-color: #fff;
        top: 0;
        left: 0;
        right: 0;
        padding: 18px;
        z-index: 999;
    }
}
   
</style>
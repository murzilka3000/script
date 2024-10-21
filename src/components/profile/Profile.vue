

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
    </div>
</template>


<style module>

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
   }
 
 
</style>
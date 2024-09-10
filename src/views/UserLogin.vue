<script setup lang="ts">

import InputText from 'primevue/inputtext';
import Password from 'primevue/password';
import { ref } from 'vue';

const username = defineModel<string>('username')
const password = defineModel<string>('password')


</script>

<template>
    <div class="login_container">
        <div class="credentials">
            <div class="username">
                <FloatLabel>
                    <label for="username">Usuário</label>
                    <InputText type="text" v-model="username" placeholder="Usuário"/>
                </FloatLabel>
            </div>
            <div class="password">
                <FloatLabel>
                    <label for="password">Senha</label>
                    <Password v-model="password" :feedback="false" placeholder="Senha" />
                </FloatLabel>
            </div>
        </div>
        <div class="forgotPassword">
            <a href='http://localhost:5173/' target='conteudo'>Esqueceu a senha?</a>
        </div>
    </div>
</template>

<style scoped lang="scss">

.login_container {
    position: relative;
    left: 200%;
    display: flex;
    flex-direction: column;
    width: 250px;
    height: 500px;
    justify-content: space-around;
    align-items: center;
}

.username, 
.password {
    margin-bottom: 30px;
}


.crendentials {
    position: relative;
    border: white;
}

.p-inputtext {
    width: 200px;
    height: 25px;
    border: 1px solid #ffffff;
    display: block;
    flex-direction: column;
}

.p-password {
    width: 200px;
    height: 25px;
    border: 1px solid #ffffff;
    flex-direction: column;
    display: flex;
    position: relative;
}

.p-password-input {
    width: 100%;
    height: 100%;
    border: 1px solid #ffffff;
    flex-direction: column;
    display: flex;
    position: relative;
}

</style>
<template>
    <form  class="login-card">
        
        <div class="text">Login to your account</div>


        <div class="email" id="login-input">
            <label class="text-white text-sm font-normal" for="email">Email</label>
            <DxTextBox placeholder="Email Address..">
                <DxValidator>
                    <DxRequiredRule />
                    <DxEmailRule />
                </DxValidator>
            </DxTextBox>
        </div>

        <div class="pass" id="pass">
            <label class="text-white text-sm font-normal" for="password">Password</label>
            <DxTextBox ref="passwordRef" mode="password" placeholder="Password.." >
                <DxValidator>
                    <DxRequiredRule />
                </DxValidator>
                <DxTextBoxButton name="password-button" location="after" />
            </DxTextBox>
        </div>

        <div>
            <DxButton text="Login"/>
        </div>

        <!-- <button @click="onFormSubmit">Login</button> -->

        <RouterLink to="/about">Login</RouterLink>

        
    </form>
   
</template>

<script setup lang="ts">
import { computed, ref, onMounted } from 'vue';
import { useRouter } from 'vue-router';
import { DxButton, DxButton as DxTextBoxButton, DxTextBox } from 'devextreme-vue/text-box';

const passwordRef = ref<DxTextBox>();

const router = useRouter();

// const onFormSubmit = () => {
 
//             // redirect to home
//             router.push({ path: '/about' });
       
// };

</script>

<style>
.text{
    padding: 2rem;
}
.login-card{
    background-color: rgba(255, 255, 255, 0.4);
    border-radius: 5px;
    width: 70vh;
    margin-left: 50rem;
    text-align: center;
    margin-top: 5rem;
}

.email{
    margin-left: 3rem;
    width: 50vh;
}

.pass{
    margin-left: 3rem;
    width: 50vh;
    padding-bottom: 2rem;
}

</style>

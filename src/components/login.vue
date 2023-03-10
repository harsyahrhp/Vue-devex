<template>
    <div class="login-card">
        <form>
            <div class="name">
            <label for="Name">Name</label>
            <input type="Name">
            </div>

            <div class="password">
            <label for="password">Password</label>
            <input type="password">
            </div>

            <div class="mb-3.5" id="login-input">
            <label class="text-white text-sm font-normal" for="email">Email</label>
            <DxTextBox placeholder="Email Address..">
                <DxValidator>
                    <DxRequiredRule />
                    <DxEmailRule />
                </DxValidator>
            </DxTextBox>
        </div>
            
            <button><a href="/meratus">Login</a></button>
        </form>
    </div>    
</template>

<style>
.login-card{
    background-color: rgba(255, 255, 255, 0.4);
    border-radius: 5px;
    width: 70vh;
    margin-left: 50rem;
    text-align: center;
    margin-top: 5rem;
}

input{
    border-radius: 2px;
}

form{
    padding: 2rem;
}

.name{
    padding: 2rem;
}

label{
    margin: 2rem;
}

button{
    background-color: navy;
}
</style>
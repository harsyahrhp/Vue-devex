<template>
    <nav>
    <div class="Navbar">
        <div class="right">
            <img src="src/assets/Image/favicon.ico" alt="">
            <span>MeratusLine</span> 
        
        </div>
      
        <div class="left">
            <RouterLink to="/">Login</RouterLink>
            <RouterLink to="/Meratus">Chart</RouterLink>
            <RouterLink to="/about">product</RouterLink>
        </div>

        
    </div>
    </nav>
</template>

<style>
    .Navbar{
        color: white;
        display: flex;
        justify-content: space-between;
    }

    .left a{
        padding: 2rem;
    }

    img{
        width: 60px;
    }

    .right{
        font-size: 30px;
        display: flex;
    }

    nav{
        background-color: navy;
        padding: 2rem;
    }
</style>
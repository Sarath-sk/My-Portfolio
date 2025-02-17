<template>
    <header class="header">
            <div class="user" style="font-size:1.5rem">Sarath Kumar Yeduru</div>
            <div class="menu-toggle" id="menuToggle" @click="toggleMenu">
                <div class="line" :class="{'active':menuVisible}"></div>
                <div class="line" :class="{'active':menuVisible}"></div>
                <div class="line" :class="{'active':menuVisible}"></div>
            </div>
            <nav class="navigation">
                <ul>
                    <li><router-link to="/">Home</router-link></li>
                    <li><router-link to="/about">About</router-link></li>
                    <li><router-link to="/experience">Experiences</router-link></li>
                    <li><router-link to="/projects">Projects</router-link></li>
                    <li><router-link to="/github">GitHub</router-link></li>
                    <li><router-link to="/contact">Contact</router-link></li>
                </ul>
            </nav>

            <nav v-if="menuVisible" class="navigation_mobile">
                <ul>
                    <li>Home</li>
                    <li>About</li>
                    <li>Experiences</li>
                    <li>Projects</li>
                    <li>GitHub</li>
                    <li>Contact</li>
                </ul>
            </nav>
        </header>
</template>

<style scoped>
.user{
    background: linear-gradient(to right, #a18c37, #bb343d);
    -webkit-background-clip: text;
    color: transparent;
}

header{
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    background-color: #033353;
    position: fixed;
    left: 0;
    top: 0;
    width: 100dvw;
    padding: 0.5rem;
    color: white;
    box-shadow: 0px 7px 10px rgba(9, 14, 67, 0.8)

}

.navigation > ul{
    list-style: none;
    display: flex;
    flex-direction: row;
    gap: 1.5rem;
    background-color: inherit;
}
.navigation a.router-link-exact-active {
  color: #42b983;
}
.navigation a {
  color: white;
}

.navigation a{
    text-decoration: none;
}

.navigation_mobile{
    display: none;
}

@media (max-width: 660px){
    nav.navigation{
        display: none;
    }

    #menuToggle{
        display: flex;
    }

    .navigation_mobile{
        display: block;
        transform: translateX(0);
        background-color: #033353;
        margin-top: 4rem;
        width: 100dvw;
        height: 20rem;
        position: fixed;
        top: 0;
        left: 0;
        padding: 1rem;
        
    }

    nav.navigation_mobile ul{
        display: flex;
        flex-direction: column;
        gap: 1rem;
        
        list-style-type: none;
        padding: 0;
        margin: 0;
        height: 100%;
    }

    nav.navigation_mobile ul li{
        background-color:white;
        border-radius: 0.2rem;
        padding: 0.5rem;
        color: #033353;
        /* border-bottom: 1px solid white; */
    }

    nav.navigation_mobile ul li:hover{
        cursor: pointer;
        color: #9F5255;
    }

    #menuToggle{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width: 2.3rem; 
        height: 1.7rem;
        cursor: pointer;
    }

    .line{
        width: 100%;
        height: 0.2rem; 
        background-color: #f7f5f5;
        border-radius: 0.2rem;
    }

    h1{
        padding: 3rem;
        background-color: #033353;
        color: white;
        width: 100%;  
    }

    .active{
    background-color: #FFB22C;
}

}
</style>
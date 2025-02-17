<template>
    <Header/>
    <div class="home">
        
        <section>
            <h1>{{currentTime}} guys, Welcome back &#x1F44B;</h1>
            <div class="data-container">
                <div class="q-dataitem">
                    <h2 class="user">Hi, I'm Sarath Kumar Yeduru</h2>
                    <h4>Software Development Engineer in Test - SDET</h4>
                </div>
                <div class="q-dataitem">
                    <p>Higly skilled Automation Developer with 3 years of Experience in implementing and designing feasible Automation Frameworks. Profficient in Java, Python and C# along with Playwright and Selenium Automation tools.</p>
                </div>
                <div class="q-dataitem">
                    <p>Expert in automating Web applications using JUnit, TestNG, Pytest, NUnit and Cucumber frameworks and Mobile applications using Appium. Familiar with SCRUM, Agile methodologies using Azure Devops and Jira.</p>
                </div>
            </div>
        </section>
        
    </div>
    <Footer/>
</template>

<script>
import Header from '../components/Header.vue';
import Footer from '../components/Footer.vue'
export default {
    name:'HomePage',
    components:{
        Header,
        Footer
    },
    data(){
        return{
            menuVisible: false,
            currentYear: new Date().getFullYear(),
            currentTime: this.getCurrentTime()
        };
    },
    methods:{
        toggleMenu() {
            this.menuVisible = !this.menuVisible;
        },
        getCurrentTime(){
            const now = new Date()
            const hours = now.getHours()
            
            if (hours >= 0 && hours < 12) {
                return "Good Morning!";
            } else if (hours >= 12 && hours < 17) {
                return "Good Afternoon!";
            } else {
                return "Good Evening!";
            }
        }
    }
};

</script>

<style scoped>

* {
    margin: 0%;
    padding: 0%;
    box-sizing: border-box;
}

.user{
    background: linear-gradient(to right, #a18c37, #bb343d);
    -webkit-background-clip: text;
    color: transparent;
    font-size: 2.5rem;
}

.home{
    margin-top: 4rem;
    height: 100%;
}

h1{
    padding: 2rem;
    background-color: #033353;
    color: white;
    width: 100%;   
}



.data-container{
    background-color: #23486A;
    color: white;
    padding: 8rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

.q-dataitem{
    display: flex;
    flex-direction: column;
    text-align: center;
    margin: 0 15rem;
    align-content: center;
}





@media (max-width: 900px){
    .q-dataitem{
        margin: 0 10rem;
    }

    footer{
        display: flex;
        flex-direction: row;
        gap: 0.2rem;
    }
}

@media (max-width: 560px){
    .q-dataitem{
        margin: 0 2rem;
    }
    footer{
        display: flex;
        flex-direction: row;
        gap: 0.2rem;
    }
}

</style>

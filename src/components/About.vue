<template>
    <Header/>
    <div class="about">
        <section>
            <div class="profile-container">
                <img src="../assets/Photo.jpg" alt="profile">
            </div>
            <div class="user-container">
                <h1>Sarath Kumar</h1>
                <p>Software Development Engineer in Test - SDET</p>
            </div>
            <div class="roles-container">
                <h2>Roles & Responsibilities</h2>
                <div>
                    <p>Designing and developing automated test scripts using programming languages (Java, Python, C#, etc.).</p>
                    <p>Creating test frameworks and tools for efficient and scalable testing.</p>
                    <p>Maintaining and updating existing automated test scripts.</p>
                    <p>Working alongside developers to understand the functionality, architecture, and design of the application.</p>
                    <p>Documenting detailed bug reports and collaborating with developers to reproduce and resolve issues.</p>
                </div>
            </div>
            <div class="skills-container">
                <h2>Skills & Technologies</h2>
                <div>
                    <div class="items-container">
                        <h4>Programming Languages</h4>
                        <div class="items">
                            <span>Java</span><span>Python</span><span>C#.NET</span>
                        </div>
                    </div>
                    <div class="items-container">
                        <h4>Automation Tools</h4>
                        <div class="items">
                            <span>PlayWright</span><span>Selenium</span><span>Appium</span><span>JMeter</span><span>POM</span>
                        </div>
                    </div>
                    <div class="items-container">
                        <h4>Automation Frameworks</h4>
                        <div class="items">
                            <span>Pytest</span><span>TestNG</span><span>Cucumber(BDD)</span><span>JUnit</span><span>NUnit</span><span>Healenium</span>
                        </div>
                    </div>
                    <div class="items-container">
                        <h4>Web Technologies</h4>
                        <div class="items">
                            <span>HTML</span><span>CSS</span><span>Javascript</span><span>Vue.js</span><span>React.js</span>
                        </div>
                    </div>
                    <div class="items-container">
                        <h4>Version Control Systems</h4>
                        <div class="items">
                            <span>Git</span><span>Azure DevOps</span>
                        </div>
                    </div>
                </div>
            </div>
            
        </section>
    </div>
    <Footer/>
</template>



<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
export default {
    components:{
        Header,
        Footer
    }
}
</script>


<style scoped>
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    background-color: #23486A;
}
.about{
    padding: 5rem;
}

img{
    width: 15rem;
    height: 15rem;
    border: 0.3rem solid #A0C878;
    border-radius: 10rem;
}

section{
    display: flex;
    flex-direction: column;
    text-align: center;
    gap: 2rem;
    /* background-color: #23486A; */
    color: white;
}

h2{
    color: #72BAA9;
}
h4{
    color: whitesmoke;
}

.roles-container{
    display: flex;
    flex-direction: column;
}

.roles-container > div{
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.skills-container{
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.skills-container > div{
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

.items-container{
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

.items-container > div{
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 1rem;
}

.items > span{
    border: 0.1rem solid black;
    padding: 0.4rem;
    background-color: #808b97;
    border-radius: 0.4rem;
}


</style>
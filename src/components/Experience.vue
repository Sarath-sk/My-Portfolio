<template>
<Header/>
<div class="experience">
    <section>
        <h2>Work Experience &#x1F4BC;</h2>

        <div class="work-history">
            <div>
                <h3>Software Development Engineer in Test - SDET</h3>
                <h4>Revolution Entertainment Services</h4>
                <p>August 2024 - Present</p>
                <ul>
                    <li>Designed and implemented a robust automation framework from the ground up for the 
ProHire web application, enabling efficient execution of high-priority test cases and automated 
report generation. </li>
                    <li>Built and deployed a Playwright-based framework in Python for the ProHire mobile web 
application, streamlining and ensuring a smooth, error-free employee onboarding experience. </li>
                    <li>Responsible for end-to-end testing to assure and deliver defect free application</li>
                </ul>
            </div>
            <div>
                <h3>Automation Test Enginner</h3>
                <h4>Tata Consultancy Services</h4>
                <p>December 2021 - August 2024</p>
                <ul>
                    <li>Developed a well structured automation framework for SharePoint web project from scratch, 
to run high priority test cases along with report generation.</li>
                    <li> Integrated Healenium into the project framework, allowing scripts to self-heal and 
subsequently diminishing the requirement for the code maintenance. </li>
                    <li>Responsible to deliver defect free product by performing end-to-end testing along with Regression testing.</li>
                </ul>
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
    color: white;
}

section{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    margin: 0 10rem;
    gap: 2rem;
}

.work-history{
    display: flex;
    flex-direction: column;
    justify-content: start;
    text-align: start;
    gap: 2rem;
}

h3{
    color: #00bbf0;
}

.work-history > div {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    padding: 1rem;
    border-left: 0.3rem solid #42b983;
}

.work-history > div > ul{
    margin-left: 1rem;
}

.work-history > div > p{
    font-style: italic;
}
.experience{
    padding: 5rem;
}
h2{
    color: #72BAA9;
}
</style>
<template>
    <Header/>
    <div class="projects">
        <section>
            <div>
                <h1>My Projects &#x1F680;</h1>
                <h5>A collection of projects I've worked on professionally.</h5>
            </div>
            <div class="projects-container">
                <div class="container-item">
                    <h2>ProHire</h2>
                    <p>Web-based employee onboarding and timecard application.</p>
                    <div>
                        <span><strong>Company:</strong> Revolution Entertainment Services,</span>
                        <span>Hyderabad</span>
                        <span><strong>Role:</strong> SDET</span>
                    </div>
                    <div>
                        <p>ProHire is the industry leading web-based employee onboarding and timecard application for Commercials, Features and TV.</p>
                    </div>
                </div>
                <div class="container-item">
                    <h2>SetKeeper</h2>
                    <p>Web-based access control,personalized distribution, security and tracking.</p>
                    <div>
                        <span><strong>Company:</strong> Revolution Entertainment Services,</span>
                        <span>Hyderabad</span>
                        <span><strong>Role:</strong> SDET</span>
                    </div>
                    <div>
                        <p>SetKeeper is the new web-based application for all in one of digital crew onboarding, timecard calculation, production distribution, access control and water marking. </p>
                    </div>
                </div>
                <div class="container-item">
                    <h2>Microsoft SharePoint Administrator</h2>
                    <p>Managing, configuring, and maintaining SharePoint environments to ensure optimal performance, security, and usability.</p>
                    <div>
                        <span><strong>Company:</strong> Tata Consultancy Services,</span>
                        <span>Hyderabad</span>
                        <span><strong>Role:</strong> Automation Test Engineer</span>
                    </div>
                    <div>
                        <p>A Microsoft SharePoint Administrator is responsible for managing, configuring, and maintaining SharePoint environments to ensure optimal performance, security, and usability. SharePoint admins play a critical role in enabling organizations to leverage SharePoint for collaboration, document management, and business processes.</p>
                    </div>
                </div>
                <div class="container-item">
                    <h2>Microsoft Office</h2>
                    <p>It is one of the most widely used software suites in the world, catering to individuals, businesses, and educational institutions.</p>
                    <div class="">
                        <span><strong>Company:</strong> Tata Consultancy Services,</span>
                        <span>Hyderabad</span>
                        <span><strong>Role:</strong> Automation Test Engineer</span>
                    </div>
                    <div>
                        <p>Microsoft Office is a suite of productivity applications developed by Microsoft. It is one of the most widely used software suites in the world, catering to individuals, businesses, and educational institutions. Microsoft Office provides tools for creating, editing, managing, and sharing documents, presentations, spreadsheets, emails, and more.</p>
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
    color: white;
    
}

h1{
    color: #72BAA9;
}

template{
    background-color: #23486A;
}

.projects{
    padding: 5rem;
}

section{
    display: flex;
    flex-direction: column;
    gap: 2rem;
    justify-content: center;
    align-items: center;
}

.projects-container{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
    justify-content: center;
    align-items: center;
    
}

strong{
    color: #c7b198;
}

.container-item{

    border-radius: 1rem;
    width: 30rem;
    height: 25rem;
    text-align: start;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap:1rem;
    background-color: #00204a;

}


.container-item > div{
    display: flex;
    flex-direction: column;
    gap: 0.2rem;
    background-color: inherit;
}

h2{
    color: #00bbf0;
}

@media (max-width:1015px){
    .container-item{
        width: 25rem;
        height: 20rem;
    }
}

@media (max-width: 860px){
    .container-item{
        width: 20rem;
        height: 35rem;
    }
}

@media (max-width: 690px){
    .container-item{
        width: 25rem;
        height: 26rem;
    }

    .projects-container{
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        gap: 2rem;
        justify-content: center;
        align-items: center;
    
    }
}

@media (max-width: 415px){
    .container-item{
        width: 20rem;
        height: 35rem;
    }
}

</style>
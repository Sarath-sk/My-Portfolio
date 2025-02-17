<template>
    <Header/>
    <div class="contact">
        <section>
            <div>
                <h1>Get in Touch &#x1F4DE;</h1>
                <h5>Let's connect and collaborate. Fill out the form below or reach me via social media.</h5>
            </div>
            <div class="contact-container">
                <p><Strong>Email:</Strong> sarath.yeduru@gmail.com</p>
                <p><Strong>Mobile:</Strong> +91 6304987684</p>
                <p><strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/sarathyeduru/"> Here</a></p>
                <a href="src\assets\resume.pdf" download="Sarath_Kumar_Resume.pdf">
                    <button style="color:black;">
                        Resume &#x1F4E5;
                    </button>
                </a>

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

.contact{
    padding: 5rem;
}

h1{
    color: #72BAA9;
}

strong{
    color: #c7b198;
}

section{
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

.contact-container{
    display: flex;
    flex-direction: column;
    border-radius: 0.5rem;
    margin: 5rem 10rem;
    justify-content: center;
    align-content: center;
    height: 15rem;
    gap: 2rem;
    background-color: #00204a;
}

button{
    width: 6rem;
    height: 2.5rem;
    font-weight: bold;
}

@media (max-width: 770px){
    .contact-container{
        margin: 0 2rem;
    }
    
}

@media (max-width: 470px){

    .contact-container{
        margin: 2rem 0.1rem;
    }

    
}

@media (max-width: 400px){

    .contact-container{
        margin: 2rem 0.1rem;
    }

    .contact{
        margin-top: 4rem;
        padding: 2rem;
    }

    
}
</style>

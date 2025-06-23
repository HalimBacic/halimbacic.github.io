<template>
    <div class="maincontainer">
        <div class="navigation">
            <a href="/files/HalimBacicCV.pdf" target="_blank" class="nav-link-reset">
                <div class="navbtn">My CV</div>
            </a>
            <a href="/files/HalimBacicCV.pdf" download="HalimBacicCV.pdf" class="nav-link-reset">
                <div class="navbtn">Download CV</div>
            </a>
        </div>
        <div class="middle">
            <div class="imagecont">
                <img src="../assets/cvslika.jpg" class="image">
            </div>
            <div class="about">
                <div style="display: flex; flex-direction: column; padding: 0.5px;">
                    <p class="text" id="firsttext">I am Halim</p>
                    <!-- <p class="text smallertext">Software engineer</p> -->
                    <p class="text secondtext">You need <i>software developer</i><span
                            style="color: red; font-family: Inter Tight, sans-serif ;font-weight: 700"> ?</span>
                    </p>
                    <p class="text secondtext">Contact me<span
                            style="color: red;  font-family: Inter Tight, sans-serif ;font-weight: 700">!</span></p>
                </div>
            </div>
        </div>
        <div class="info">
            <div class="contacts">
                <div class="contactbtn" @click="openLinkedIn()"><i class="fa-brands fa-linkedin"></i></div>
                <div class="contactbtn" @click="openGitHub()"><i class="fa-brands fa-square-github"></i></div>
                <div class="contactbtn" @click="openEmail()"><i class="fa-solid fa-envelope"></i></div>
                <div class="stackbtn stackbtnsmall">bacich95@gmail.com</div>
            </div>
            <div class="stack">
                <div class="stackbtn">Java</div>
                <div class="stackbtn">Spring</div>
                <div class="stackbtn">.NET</div>
                <div class="stackbtn">Python</div>
                <div class="stackbtn">React</div>
                <div class="stackbtn">MySQL</div>
                <div class="stackbtn">Android</div>
            </div>
        </div>
    </div>
</template>

<script setup>

const openGitHub = () => {
    // Zameni sa svojim GitHub profilom
    window.open('https://github.com/HalimBacic', '_blank');
};

const openLinkedIn = () => {
    // Zameni sa svojim LinkedIn profilom
    window.open('https://www.linkedin.com/in/halimbacic/', '_blank');
};

const openEmail = () => {
    // Zameni sa svojom email adresom
    window.open('mailto:bacich95@gmail.com');
};

</script>

<style>
html,
body,
#app {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    overflow: hidden;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
    background-color: #495E57;
}
</style>

<style scoped>
.maincontainer {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
}

.navigation {
    width: 100%;
    height: 10vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.navbtn {
    margin: 2%;
    font-family: "Matangi", sans-serif;
    font-optical-sizing: auto;
    font-weight: 800;
    color: #F4CE14;
}

.navbtn:hover {
    cursor: pointer;
}

.middle {
    display: flex;
    flex-direction: row;
    height: 80vh;
}

    .contacts {
        display: flex;
        flex-direction: row;
        height: 100%;
        margin: 2%;
        color: white;
        justify-content: center;
        align-items: center;
        flex-grow: 1;
    }

.contactbtn {
    margin: 2%;
    font-size: 2rem;
}

.contactbtn:hover {
    cursor: pointer;
}

.imagecont {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 1.5rem;
    box-sizing: border-box;
}

.image {
    border-radius: 50%;
    border: 2px solid #F4CE14;
    width: auto;
    height: auto;
    min-width: 45vh;
    max-width: 45vh;
    min-height: 35vh;
    max-height: 45vh;
    object-fit: cover;
    display: block;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}


.nav-link-reset {
    text-decoration: none;
    color: inherit;
    display: block;
    width: 20%;
}

.about {
    flex: 2;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 1.5rem;
    box-sizing: border-box;
}

.text {
    font-family: "Inter Tight", sans-serif;
    font-weight: 700;
    margin: 1px;
}

#firsttext {
    font-size: 7rem;
    color: #F4CE14;
    margin-bottom: 0px;
}

.secondtext {
    font-size: 3rem;
    color: #F5F7F8;
}

.smallertext {
    font-size: 2rem;
    font-style: italic;
    color:#F5F7F8;
}

.info {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    height: 10vh;
    background-color: #3C524B;
    align-items: center;
    padding: 0 2%;
}

.stack {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    flex-grow: 1;
}

.stackbtn {
    color: #F5F7F8;
    font-family: "Matangi", sans-serif;
    margin: 0 1%;
    font-size: 1rem;
    white-space: nowrap;
}

.stackbtnsmall {
    color: #F5F7F8;
    font-family: "Matangi", sans-serif;
    margin: 0 1%;
    font-size: 0.8rem;
    white-space: nowrap;
}

@media screen and (max-width: 768px) {
    .middle {
        display: flex;
        flex-direction: column;
        height: 100vh;
    }

    #firsttext {
        font-size: 6rem;
        color: #F4CE14;
    }

    .secondtext {
        font-size: 2rem;
        color: #F5F7F8;
    }

    .image {
        border-radius: 50%;
        border: 1px solid #F4CE14;
        width: auto;
        height: auto;
        min-width: 25vh;
        max-width: 25vh;
        min-height: 15vh;
        max-height: 25vh;
        object-fit: cover;
        display: block;
        box-shadow: 0 2px 13px rgba(0, 0, 0, 0.2);
    }

    .contacts {
        display: flex;
        flex-direction: row;
        height: 100%;
        margin: 2%;
        color: white;
        justify-content: center;
        align-items: center;
        flex-grow: 1;
    }

    .contactbtn {
        margin-left: 15%;
        margin-right: 15%;
        font-size: 2rem;
    }

    .info {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        height: 10vh;
        background-color: #3C524B;
        align-items: center;
        padding: 0 2%;
    }

    .info {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        height: 10vh;
        background-color: #3C524B;
        align-items: center;
        padding: 0 2%;
    }
}
</style>
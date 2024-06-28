HTML 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Swift Portfolio</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="mediaqueries.css">
</head>
<body>
    <nav id="desktop-nav">
<div class="logo">PureWeb</div>
<div>
    <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#Experience">Experience</a></li>
        <li><a href="#Projects">Projects</a></li>
        <li><a href="#Contact">Contact</a></li>
    </ul>
</div>
  </nav>
  <nav id="hamburger-nav">
  <div class="logo">Pure Web</div>
  <div class="hamburger-menu">
    <div class="hamburger-icon" onclick="toggleMenu()">
        <span></span>
        <span></span>
        <span></span>
    </div>
    <div class="menu-links">
        <li><a href="#about" onclick="toggleMenu()">About</a></li>
        <li><a href="#Experience" onclick="toggleMenu()">Experience</a></li>
        <li><a href="#Projects" onclick="toggleMenu()">Projects</a></li>
        <li><a href="#Contact" onclick="toggleMenu()">Contact</a></li>
    </div>
  </div>
</nav>
<section id="profile">
    <div class="section__pic-container">
        <img src="/images/999.png" alt="Hero Profile Pic">
    </div>
    <div class="section__text">
    <p class="section__text__p1">Hello,</p>
    <h1 class="section__text__p2">This is PureWeb</h1>
    <p class="section__text__p2">Transforming Visions into Digital Reality with PureWeb – Your Premier Web Development Partner.</p>
    <div class="btn-container">
    <button class="btn btn-color-1" onclick="location.href='./#Contact'"> 
        Contact Us
    </button>
    </div>
    <div id="socials-container">
        <img src="./images/instagram.png" alt="Our Instagram Profile" 
        class="icon" onclick="location.href='https://www.instagram.com/swiftlywebservices/'">
    </div>            
</section>

     <section id="about"> 
      <p class="section__text__p1">Get To Know More </p>
      <h1 class="title">About Us</h1>
      <div class="section-container">
          <div class="section__pic-container">
         <img src="/images/bckk (1).png" alt="Profile picture" 
         class="about-pic"
         />
        </div>
        <div class="about-details-container">
             <div class="about-containers">
                <div class="details-container">
                    <img src="/images/icons8-award-50.png"
                    alt="Experience Icon"
                    class="icon"
                    /> 
                     <h3>Experience</h3>
                      <p>2+ years <br />Frontend Development</p>
                </div>
                <div class="details-container">
                    <img src="/images/icons8-education-80.png"
                    alt="Education Icon"
                    class="icon"
                    />
                    <h3>Developing Languages</h3>
                    <p>HTML & CSS<br />Javascript</p> 
                </div>
            </div>
                 <div class="text-container">
                <p>Welcome to PureWeb, your dedicated team of expert web developers committed to bringing your digital vision to life. At PureWeb,
                 we blend creativity with cutting-edge technology to craft websites that are not only visually stunning but also highly functional and user-friendly. Our team of skilled professionals specializes in responsive design, seamless user experiences, and robust backend solutions, ensuring your online presence stands out in today’s competitive landscape. Trust PureWeb to deliver exceptional results, tailored to meet your unique business needs.
                </p>
            </div>
        </div>
    </div>
    <img src="/images/icons8-down-arrow-50.png" alt="Arrow icon" class="icon arrow" onclick="location.href='./#Experience'" />
     </section>
   
   




    
 <script src="script.js"></script>   
</body>
</html>










CSS

/* GENERAL */

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap');

* {
    margin: 0;
    padding: 0;
}

body {
    font-family: "Poppins", sans-serif;

}

html{
    scroll-behavior: smooth;

}

p {
    color: rgb(85,85,85);
}

/* TRANSITION */

a, .btn {
    transition: all 300ms ease
}

/* DESKTOP NAV*/


nav, .nav-links {
    display:flex;
}

nav {
    justify-content: space-around;
    align-items: center; 
    height: 17vh;
}

.nav-links {
    gap: 2rem;
    list-style: none;
    font-size: 1.5rem;
}

a {
    color: black;
    text-decoration: none;
    text-decoration-color: white;

}

a:hover {
    color: grey;
    text-decoration: underline;
    text-underline-offset: 1rem;
    text-decoration-color: rgb(181, 181, 181);
}

.logo {
    font-size: 2rem;

}

.logo:hover{
    cursor: default;
}

/* HAMBURGER */

#hamburger-nav {
    display: none;

}

.hamburger-menu {
    position: relative;
    display: inline-block;

}

.hamburger-icon {
   display: flex;
   flex-direction: column;
   justify-content: space-between;
   height: 24px;
   width: 30px;
   cursor: pointer; 
}

.hamburger-icon span {
    width: 100%;
    height: 2px;
    background-color: black;
    transition: all 0.3 ease-in-out;
}

.menu-links {
    position: absolute;
    top: 100%;
    right: 0;
    background-color: white;
    width: fit-content;
    max-height: 0;
    overflow: hidden;
    transition: all 0.3 ease-in-out;


}

.menu-links a {
    display: block;
    padding: 10px;
    text-align: center;
    font-size: 1.5rem;
    color: black;
    text-decoration: none;
    transition: all 0.3 ease-in-out;

}

.menu-links li {
    list-style: none;

}

.menu-links.open {
    max-height: 300px;

}

.hamburger-icon.open span:first-child {
    transform: rotate(45deg) translate (10px, 5px);
}
.hamburger-icon.open span:nth-child(2) {
    opacity: 0;
}
.hamburger-icon.open span:last-child {
    transform: rotate(-45deg) translate (10px, -5px);
}

.hamburger-icon span:first-child {
    transform: none;
    
}
.hamburger-icon span:first-child {
    opacity: 1;

}
.hamburger-icon span:first-child {
    transform: none;

}

/* SECTIONS */

section {
    padding-top: 4vh;
    height: 96;
    margin: 0 10rem; 
    box-sizing: border-box;
    min-height: fit-content;
}


.section-container {
    display: flex;
}

/* PROFILE SECTION */

#profile {
    display: flex;
    justify-content: center;
    gap: 5rem;
    height: 80vh;

}

.section__pic-container {
    display: flex;
    height: 540px;
    width: 470px;
    margin: 10 0;
}

.section__text {
    align-self: center;
    text-align: center;

}

.section__text p {
    font-weight: 600;

}

.section__text__p1 {
    text-align: center;
    
}

.section__text__p2 {
    font-size: 1.75rem;
    margin-bottom: 1rem;

}

.title {
    font-size: 3rem;
    text-align: center;

}

#socials-container {
    display: flex;
    justify-content: center;
    margin-top: 1rem;
    gap: 1rem;
    
}

/* ICON */

.icon {
    cursor: pointer;
    height: 2rem;
}

/*BUTTONS*/

.btn.container {
    display: flex;
    justify-content: center;
    gap: 1rem;

}

.btn {
    font-weight: 600;
    transition: all 300ms ease;
    padding: 1rem;
    width: 8rem;
    border-radius: 2rem;

}

.btn-color-1 {
    border: rgb(53, 53, 53) 0.1rem solid;

}

.btn-color-1:hover {
    cursor: pointer;
}

.btn-color-1 {
    background: rgb(53, 53, 53);
    color: white;
}

.btn-color-1:hover {
    background: rgb(0,0,0);
}

.btn-container {
    gap: 1rem;
}

/* ABOUT SECTION */

#about {
    position: relative;
}

.about-containers {
    gap: 2rem;
    margin-bottom: 2rem;
    margin-top: 2rem;

}

.about-details-container {
    justify-content: center;
    flex-direction: column;
    

}

.about-containers, .about-details-containers {
    display: flex;
}

.about-pic {
    border-radius: 2rem;

}

.arrow {
    position: absolute;
    right: -5rem;
    bottom: 2.5rem;
    
}









<template>
    <div class="wrapper" id="home">

      <nav class="navbar" >
      <ul>
        <li><a href="#about" >About</a></li>
        <li><a href="" >Home</a></li>
        <li><a href="#portfolio" >Portfolio</a></li>
        <li><a href="#contact" >Contact</a></li>
        <li><a href="#skills" >Skills</a></li>
        <li><a href="#proj" >Projects</a></li>
      </ul>
    </nav>

    <div class="content">
        <img src="@/assets/cuyos.jpg" alt="home" class="home"/>

        

           <h1> Hello, I'm</h1>
           <p class="a">JANMARIE CUYOS</p>

        <p class ="cta">
         - A Creative Freelancer and Web Designer -
        </p>
        


    <div class="social-media">
    <a href="https://www.facebook.com/jancuyos/" target="_blank"><i class="fab fa-facebook"></i></a>
    <a href="https://twitter.com/STARC46466" target="_blank"><i class="fab fa-twitter"></i></a>
    <a href="https://www.instagram.com/janmawiekyus/" target="_blank"><i class="fab fa-instagram"></i></a>
    <!-- Add more social media icons and links as needed -->
  </div>
</div>

<div id="about" class="about">
  <center>
        <h2 > ABOUT ME </h2>
      </center>
            <p class="abc">  Hi  I am Janmarie Cuyos, a passionate BSIT student 
                  from Cordova Public College. With a background in Information of Technology 
 and currently 3 years of experience during college, I specialize in 
Web design, Graphics and Design,Installing OS (Windows10), and Web system. I'm dedicated to delivering high-quality
 work that exceeds expectations and drives results.  
          
                                                             
When I'm not coding or designing, you can find me performing in a band, yes i am a drummer my side hassle source of income. you can click the link to see my fb band page <a href ="https://www.facebook.com/landscapeofficialph">LANDSCAPE PH</a>. Support local please huhu :')
Let's connect and collaborate on your next project!   
</p>
    </div>
        

    <div id ="skills" class="c">
        <h2>Programming Languages Expertise</h2>

    <div class="grid-container">
       <div v-for="(language, index) in languages" :key="index" class="language">
          <p class="language-name">{{ language.name }}</p>

       <div class="stars-container">
          <span v-for="n in 5" :key="n" :class="{ 'filled': n <= language.expertiseLevel }">★</span>
      </div>
    </div>
  </div>
</div>


    <div id = "proj"class="ab">
      <h2>Projects</h2>

<div v-for="(link, index) in links" :key="index" class="card">
  <a :href="link.url" target="_blank">
    <img :src="link.imageUrl" alt="Link Image">
    <h2>{{ link.title }}</h2>
    <p>{{ link.description }}</p>
  </a>
</div>
    </div>

    <div id="contact" class="b">
        <h2> Contact Information </h2>

        <div class="contact">

          <div class="contact-item">
            <label for="email">Email:</label><br>
            <span id="email"><b>{{ contact.email }}</b></span>
          </div>

          <div class="contact-item">
            <label for="phone">Phone:</label><br>
            <span id="phone"><b>{{ contact.phone }}</b></span>
          </div>

          <div class="contact-item">
           <label for="address">Address:</label><br>
           <span id="address"><b>{{ contact.address }}</b></span>
         </div>
     </div>
     </div>

  </div>
  </template>
  
    
  <script>
  import exampleImage1 from '@/assets/account.png'; 
  import exampleImage2 from '@/assets/Lost.png'; 
  import exampleImage3 from '@/assets/fitness.jpg'; 
  import exampleImage4 from '@/assets/task.jpg'; 
  import exampleImage5 from '@/assets/calcu.jpg'; 
  import exampleImage6 from '@/assets/package.jpg'; 
  export default {
    data() {
      return {
        links: [
          { title: 'Lost and Found System', url: '', description: 'Lost And Found', imageUrl: exampleImage2},
          { title: 'Account Management System', url: 'https://github.com/JANMARIECUYOS/Project-IM.io', description: 'Account Management System', imageUrl: exampleImage1 },
          { title: 'Fitness Website', url: 'https://github.com/JANMARIECUYOS/FITNESS-WEBSITE-HTML.github.io', description: 'fitness website', imageUrl: exampleImage3 },
          { title: 'Task List', url: 'https://github.com/JANMARIECUYOS/todo.github.io', description: 'Task List', imageUrl: exampleImage4 },
          { title: 'Simple Calculator', url: 'https://github.com/JANMARIECUYOS/memory-function-calculator.github.io', description: 'Simple Calculator', imageUrl: exampleImage5 },
          { title: 'Package Express', url: 'https://github.com/JANMARIECUYOS/Package', description: 'Package', imageUrl: exampleImage6 }
      
        ],
        contact: {
      
          email: 'janmarie.cuyos@yahoo.com',
          phone: '09260891999/09300740464',
          address: '159 F MARTIR ST. POBLACION LAPU-LAPU CITY'
        },
        languages: [
          { name: 'JavaScript', expertiseLevel: 1 }, // Expertise level out of 5
     
          { name: 'Java', expertiseLevel: 2 },
          { name: 'C++', expertiseLevel: 3 },
          { name: 'HTML/CSS', expertiseLevel: 4 },
          { name: 'Node JS', expertiseLevel:2 },
          { name: 'PHP', expertiseLevel: 3 },
          { name: 'C#', expertiseLevel: 2 }
        ]
      };
    }
  };
  </script>
  
  
<style scoped>
h1{
  text-align: center;
}
  .wrapper {
    /* flex: 1; */
    overflow-y: auto;
    /* background: linear-gradient(to top, #ffffff, #f0f0f0, #7FD625); */
    background: #000000;
    color: #eaff2c;
  }

 .navbar li {
  display: inline;
 float: right;
 margin-right: 5%;
}

.navbar a {
  text-decoration: none;
  color: #ffeb37;
  
}
  
.content {
  margin-top: 5%;
  position: relative;
  border: 5px solid rgba(0, 0, 0, 0.5); 
  border-radius: 30px; 
  padding: 40px; 
  overflow: hidden; /* Hide overflowing content */
  /* Other styles for the content container */
}

.a {
  font-family: "Arial Rounded MT Bold", Arial, sans-serif;
  font-size: 50px;
  font-weight: bold;
  color: rgb(255, 251, 41);
}
  
.ab {
    font-family: Arial, Helvetica, sans-serif;
    letter-spacing: 1px;
    text-align: justify;
    line-height: 1.5;

}
  
.cta {
   
 margin-left: 30%;
  padding: 15px 30px; 
  width: 500px;
  font-size: 1.2em; 
  background-color: #e7f152; 
  border: none; 
  border-radius: 25px; 
 font-family: "Arial Rounded MT Bold", Arial, sans-serif;
    font-weight: bold;
    transition: background-color 0.3s ease;
    color:#000000;
}

.abc {
  font-family: Times New Roman;
  letter-spacing: 1px;
  text-align: justify;
  line-height: 1.5;
  width: 85%;
}
  

  .home {
    width: 300px; /* Set width and height to define the size of the circle */
    height: 300px;
    float: right;
    margin-left: 10px;
    border-radius: 30%; /* Make the border radius 50% to create a circle */
    overflow: hidden; /* Ensure that the image is clipped to the circular shape */
  }
 
  .about {
    text-align: center;
    margin-top: 10%;
    
  }

  h2 {
    font-family: "Arial Rounded MT Bold", Arial, sans-serif;
  font-weight: bold;
  color:rgb(224, 222, 63);
  }
  .ab {
    text-align: center;
    margin-top: 10%;
    
  }

  .b {
    text-align: center;
    margin-top: 10%;
    font-size: 40px;
    margin-bottom: 5%;
  }

  .c{
    text-align: center;
    margin-top: 10%;
  }

p {
 font-family: Times New Roman;
 font-size: 25px;
 margin-left: 8%;
 width: 80%;
 text-align: center;
 color:  #ffffff;
 letter-spacing: 2px;
}

  .card {
  background-color: #fff;
  border-radius: 80px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  padding: 15px;
  margin-bottom: 20px;
  transition: transform 0.3s ease;
  width: 50%;
  margin-left: 25%;
}

.card:hover {
  transform: translateY(-5px);
}

.card a {
  text-decoration: none;
  color: #333;
}

.card h2 {
  margin-top: 0;
}

.card p {
  margin-bottom: 0;
}

.card img {
  max-width: 30%;
 
}

.contact {
  display: flex;
  flex-wrap: wrap;
}



.contact-item {
 
  background-color: #d9e25ae7;
  border: 2px solid #000000;
  color: black;
  border-radius: 10px;
  margin-bottom: 2px;
  padding: 5px;
  font-size: 20px;
  width:20%;
  margin-left: 10%;
  font-family: Times New Roman;
  letter-spacing: 2px;
  text-align: center;
  line-height: 2;
}
.grid-container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 20px;
}


.language {
  display: flex;
  flex-direction: column;
}

.language-name {
  margin-bottom: 5px;
    font-weight: bold;
    color: #3cc07e;
}

.stars-container {
  display: flex;
  margin-left: 30%;
}

.stars-container span {
  color: #a0a0a0;
  font-size: 25px;
}

.stars-container span.filled {
  color: #ffe711; /* Change the color as per your requirement */
  
}

.social-media {
  margin-top: 10px;
 

}

.social-media a {
  margin-right: 10px;
  text-decoration: none;
  color: hsl(69, 94%, 68%); 
  margin-right: 3.2%;
  float:  right;

}

.social-media a i {
  font-size: 30px; /* Adjust the size of the icons as needed */
}
  </style>
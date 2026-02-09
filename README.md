<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Tumaini School</title>
  <style>
    body{
      font-family:Arial, sans-serif;
      margin:0;
      background color:#f4f4f4;
      }
    header{
      background :#2c7a7b;
      color:white;
      text align:center;
      padding:20px;
      }
      nav{
      background:#1a202c;
      }
      nav ul{
      list style:none;
      margin:0;
      padding:0;
      text align:center;
      }
      nav ul li{
      display:inline;
      margin:10px;
      }
      nav ul li a{
      color:white;
      text decoration:none;
      }
      section{
      padding:20px;
      margin:10px;
      background:white;
      border radius:8px;
      }
      button{
      padding:8px 12px;
      marging top:10px;
      cursor:pointer;
      }
      #gallery img{
      width:300px;
      heiht:200px;
      border radius:6px;
      }
      footer{
      text align:center;
      background:#2c7a7b;
      color:white;
      padding:10px;
      }
      @media(maxwidth:600px){
      nav ul li{
      display:block;
      margin:5px 0;
      }
      #gallery img{
      width:100%;
      height:auto;
      }
      } 
  </style>
</head>
<body>
  <header>
    <h1>Tumaini School</h1>
    <p>Building Hope Through Education</p>
  </header>
  <nav>
    <ul>
      <li><a href="#about">About</a>a></li>
      <li><a href="#programs">Programs"</a>a></li>
      <li><a href="#gallery">Gallery</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
  <main>
    <section id="about">
      <h2>About Us</h2>
      <p>
        Tumain School is dedicated to providing quality education and nurturing students to become responsible citizens.
      </p>
    </section>
    <section id="programs">
      <h2>Our Programs</h2>
      <button onclick="toggleprograms()">Show/Hide Programs</button>
      <div id="programlist">
        <ul>
          <li>Primary Education</li>
          <li>Secondary Education</li>
        </ul>
      </div>
    </section>
    <section id="gallery">
      <h2>School Gallery</h2>
      <img id="slide"
        src="https://via.placeholder.com/300x200"
        alt="School Image">
      <br>
      <button onclick="prevImage()">Previous</button>
      <button onclick="nextimage()">next</button>
    </section>
    <section id="contact">
      <h2>Contact Us</h2>
      <form onsubmit="return validateform()">
        <label>name:</label>
        <input type="text"id="name">
        <br>
        <label>Email:</label>
        <br>
        <input type="email"id="email"><br><br>
        <button type="submit">submit</button>
      </form>
    </section>
  </main>
  <footer>
    <p>&copy;2026 Tumaini School.All Rights Reserved.</p>
  </footer>
  <script>
    function toggleprograms(){
      let list=
        document.getelementbyld("programlist");
      if(list.style.display==="none"){
        list.style.display="block";
        }
      else{
        list.style.display="none";
        }
      }
    let images=[
      "https://via.placeholder.com/300x200?text=school+1",
      "https:"//via.placeholder.com/300px200?text=school+2",
      "https://via.placeholder.com/300px200?text=school+3"
    ];
    let index=0;
    function nextimage(){
      index++;
      if (index>=images.length){
        index=0;
        }
      document.getelementbyld("slide").src=images[index];
      }
    function previmage(){
      index--;
      if(index<0){
        index=images.length-1;
        }
      document.getelementbyld("slide").src=images[index];
      }
    function validateform(){
      let name=
        document.getelementbyld("name").value;
      let email=
        document.getelementbyld("email").value;
      if(name===""|| email===""){
        alert("please fill all fields");
        return false;
        }
      alert("form submitted successfully!");
      return true;
      }
  </script>
</body>
</html>

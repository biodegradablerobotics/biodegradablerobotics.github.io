<html>
<style>
  body{
    font-family:Arial;
    background: linear-gradient( rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5) ), url('Images/duckBG.jpg');
    background-repeat: no-repeat;
    background-size:cover;
    background-attachment: fixed;
    background-position: center center;
  }
  .title{
    color: white;
    font-size: min(5vw, 50px);
    font-weight: bold;
    margin: 0;
    padding: 0;
  }
  .subtitle{
    color: LightGray;
    font-size: min(2vw, 20px);
    margin: 0vw 0vw min(4vw, 40px) 0vw;
    padding: 0;
  }
  .linkrow{
    width: min(80vw, 800px);
    margin: 0 auto
  }
  .linkrow:after{
    content: "";
    display: table;
    clear: both;
  }
  .linkcolumn{
    float: center;
    width: 50%;
    height: min(8vw, 80px);
    padding: 0;
    background-repeat: no-repeat;
    background-size: auto min(3vw, 30px);
    background-position: center center;
    background-color: rgba(255, 255, 255, 0.5);
    border-radius: 10px;
    border: 2px solid white;
    margin: 0 auto;
  }
  .linkcolumn:hover .linkoverlay{
    background-color: rgba(0, 0, 0, 0.5);
  }
  .linkoverlay{
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0);
    color: white;
    font-size: 20px;
    margin: auto;
    border-radius: 10px;
  }
  .section{
    width: min(80vw, 800px);
    color: white;
    font-size: min(2vw, 20px);
    text-align: left;
    margin: 0 auto
  }
  
  .pdf{
    background-color:white;
    width: min(80vw, 800px);
    height: min(103.5vw, 1035px);
    margin: min(8vw, 80px) 0vw;
  }
  
  .galleryrow{
    width: min(80vw, 800px);
    height: min(40vw, 400px);
    margin: 0 auto min(calc(4% - 4px), 36px) auto;
    padding: 0;
    background-repeat: no-repeat;
    background-position: center center;
    background-color: rgba(255, 255, 255, 0.5);
    border: 2px solid white;
  }

  .galleryrow:hover .galleryoverlay{
    opacity: 1;
  }
  .galleryoverlay{
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    opacity: 0;
    margin: 0;
    padding: 0;
    background-position: center center;
  }
  .gallerytext{
    padding: 5%;
    color: white;
    font-size: min(2vw, 20px);
    text-align: left;
  }
  .textbutton{
    color: white;
    font-size: min(4vw, 40px);
    text-align: center;
    line-height: min(8vw, 80px);
    padding: 0;
    margin: 0;
  }
  
</style>
  
<body align="center">
 
  <p class=title align="center" style="margin: min(10vw, 100px) 0% 0% 0%">Welcome To B.I.R.B.</p>
  <p class=title align="center">Biodegradable Inspired Robotic Bird</p>
  <p class=subtitle align="center">EGR 557 Foldable Robotics Team 3</p>
  
  <div class="linkrow">
    <div class="linkcolumn" align="center" style ="background-image: url('Images/GitHub.png');">
      <a href="https://github.com/biodegradablerobotics/biodegradablerobotics.github.io"><div class=linkoverlay></div></a>
    </div>
  </div>
  
  <div class=section align="center">
    <p style="font-size: min(4vw, 40px)">Introduction</p>
    <p style="margin: 0 0 0 5%;">Chris Breaux    cbreaux1@asu.edu</p>
    <p style="margin: 0 0 0 5%;">George Muhn     gmuhn@asu.edu</p>
    <p style="margin: 0 0 0 5%;">Lien White      ljwhite8@asu.edu</p>
  </div>
  
  <div class=section align="center">
    <p style="font-size: min(4vw, 40px)">Assignments</p>
  </div>

  [Developing A Research Question](DevelopaResearchQuestion.md)

  <div class=galleryrow align="center" style="background-image: url('Images/plastic.jfif'); background-size: cover">
      <a href="DevelopaResearchQuestion" style="text-decoration:none;"> 
        <div class=galleryoverlay>
          <div class=gallerytext>
            <b>Develop a Research Question</b>
          </div>
        </div>
      </a>
  </div>

  [Bio-mechanics Background and Initial Specifications](Documents/Biomech_back_and_init_Spec.md)
  
  <div class=galleryrow align="center" style="background-image: url('Images/wingdiagram.png'); background-size: contain">
      <a href="biomechanicsbackgroundandinitialspecifications" style="text-decoration: none;">
        <div class=galleryoverlay>
          <div class=gallerytext>
            <b>Biomechanics Background and Initial Specifications</b>
          </div>
        </div>
      </a>
  </div>

  <div class=section align="center">
    <p style="font-size: min(4vw, 25px)">System Kinematics</p>
  </div>
  
  <div class=galleryrow align="center" style="background-image: url('Images/kinematics.png'); background-size: contain">
      <a href="systemkinematics.html" style="text-decoration: none;">
        <div class=galleryoverlay>
          <div class=gallerytext>
            <b>System Kinematics</b>
          </div>
        </div>
      </a>
  </div>

  <div class=section align="center">
    <p style="font-size: min(4vw, 25px)">Presentation 1</p>
  </div>
  
  <div class=galleryrow align="center" style="background-image: url('Images/presentation1.jpg'); background-size: cover">
      <a href="presentation1.html" style="text-decoration: none;">
        <div class=galleryoverlay>
          <div class=gallerytext>
            <b>Presentation 1</b>
          </div>
        </div>
      </a>
  </div>

  <div class=section align="center">
    <p style="font-size: min(4vw, 25px)">System Dynamics</p>
  </div>
  
  <div class=galleryrow align="center" style="background-image: url('Images/dynamics.png'); background-size: contain">
      <a href="systemdynamics.html" style="text-decoration: none;">
        <div class=galleryoverlay>
          <div class=gallerytext>
            <b>System Dynamics</b>
          </div>
        </div>
      </a>
  </div>

  <div class=section align="center">
    <p style="font-size: min(4vw, 25px)">Bibliography</p>
  </div>
  
  <div class="linkrow" style=" margin: min(10vw, 100px) auto">
    <div class="linkcolumn" align="center" style="width: 50%;">
      <a href="https://github.com/biodegradablerobotics/biodegradablerobotics.github.io/blob/main/Documents/Bibliography.md" style="text-decoration: none;">
        <div class=linkoverlay><p class="textbutton">Bibliography</p></div>
      </a>
    </div>
  </div>
  
  
</body>
</html>

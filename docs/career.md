<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>

:root {
    --primary-color:rgb(47, 51, 68);
}

/* The actual timeline (the vertical ruler) */
.timeline {
  position: relative;
  max-width: 1200px;

  margin: 0 auto;
}

/* The actual timeline (the vertical ruler) */
.timeline::after {
  content: '';
  position: absolute;
  width: 6px;
  background-color: var(--primary-color);
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -3px;
}

/* Container around content */
.container {
  padding: 10px 40px;
  position: relative;
  width: 50%;
}

/* The circles on the timeline */
.container::after {
  content: '';
  position: absolute;
  width: 25px;
  height: 25px;
  right: -13px;
  background-color: white;
  border: 4px solid #FF9F55;
  top: 15px;
  border-radius: 50%;
  z-index: 1;
}

/* Place the container to the left */
.left {
  left: 0;
}

/* Place the container to the right */
.right {
  left: 50%;
}

/* Add arrows to the left container (pointing right) */
.left::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  right: 30px;
  border: medium solid var(--primary-color);
  border-width: 10px 0 10px 10px;
  border-color: transparent transparent transparent var(--primary-color);
}

/* Add arrows to the right container (pointing left) */
.right::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  left: 30px;
  border: medium solid white;
  border-width: 10px 10px 10px 0;
  border-color: transparent var(--primary-color) transparent transparent;
}

.image {
  width:50px;
  height:50px;
  margin-right: 10px;
}

/* Fix the circle for containers on the right side */
.right::after {
  left: -13px;
}

/* The actual content */
.content {
  padding: 20px 30px;
  background-color:var(--primary-color);
  position: relative;
  border-radius: 6px;
}

/* Media queries - Responsive timeline on screens less than 600px wide */
@media screen and (max-width: 600px) {
  /* Place the timelime to the left */
  .timeline::after {
  left: 31px;
  }
  
  /* Full-width containers */
  .container {
  width: 100%;
  padding-left: 70px;
  padding-right: 25px;
  }
  
  /* Make sure that all arrows are pointing leftwards */
  .container::before {
  left: 60px;
  border: medium solid white;
  border-width: 10px 10px 10px 0;
  border-color: transparent white transparent transparent;
  }

  /* Make sure all circles are at the same spot */
  .left::after, .right::after {
  left: 1px;
  }
  
  /* Make all right containers behave like the left ones */
  .right {
  left: 0%;
  }
}
</style>
</head>
<body>

<div class="timeline">
  <div class="container left">
    <div class="content">
      <h4><img src="https://www.sap.com/aemedge/icons/sap-logo.svg" class="image">Dec 2020 – Present</h4>
      <p>Development Architect</p>
    </div>
  </div>
  <div class="container right">
    <div class="content">
     <h4><img src="https://www.eon.de/content/dam/eon/eon-de-zwei/svg-mein-eon/logo-eon-red.svg" class="image">Jul 2019 – Nov 2020</h4>
      <p>Android Lead Developer</p>
    </div>
  </div>
  <div class="container left">
    <div class="content">
     <h4><img src="https://upload.wikimedia.org/wikipedia/de/thumb/7/74/Joyn_%28Streaminganbieter%29_logo.svg/1600px-Joyn_%28Streaminganbieter%29_logo.svg.png?20191126194036"class="image"> Mar 2019 – Jun 2019</h4>
      <p>Senior Android Developer</p>
    </div>
  </div>
  <div class="container right">
    <div class="content">
      <h4><img src="https://look.ams-osram.com/transform/2f3e8012-68d3-4dc2-8719-14e23820a091/Logo-rgb-without-bounding-box-orange-transparent-background?" class="image"/>Mar 2018 – Feb 2019</h4>
      <p>Senior Android Developer</p>
    </div>
  </div>
  <div class="container left">
    <div class="content">
      <h4><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/Westwing_Logo_03.2021.svg/562px-Westwing_Logo_03.2021.svg.png" class="image"/>Oct 2014 – Feb 2018</h4>
      <p>Senior Android Developer</p>
    </div>
  </div>
</div>
</body>
</html>
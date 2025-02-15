<html>
<head>
<meta name="viewport" content="width=device-width initial-scale=1.0">

<style>

:root {
    --primary-color: #e1e2ea;
}

/* Dark Mode */
[data-md-color-scheme="slate"] {
    --primary-color: #2f3344;
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
  background-color:rgb(139, 191, 139);
  border: 5px solid var(--primary-color);
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
  border: medium solid var(--primary-color);
  border-width: 10px 10px 10px 0;
  border-color: transparent var(--primary-color) transparent transparent;
  }

  /* Make sure all circles are at the same spot */
  .left::after, .right::after {
  left: 18px;
  }
  
  /* Make all right containers behave like the left ones */
  .right {
  left: 0%;
  }

.centered-text {
            display: flex;
            justify-content: center;
            align-items: center; 
            text-align: center;

}
</style>
</head>
<body>

<div class="centered-text">
    <h3>Germany 🇩🇪</h3>
</div>

<hr >
<div class="timeline">
  <div class="container left">
    <div class="content">
      <h2><img src="https://www.sap.com/aemedge/icons/sap-logo.svg" class="image" alt="SAP">SAP</h2>
      <h6>DEC 2020 – PRESENT</h6>
      <p>Development Architect</p>
    </div>
  </div>
  <div class="container right">
    <div class="content">
     <h2><img src="https://www.eon.de/content/dam/eon/eon-de-zwei/svg-mein-eon/logo-eon-red.svg" class="image" alt="E.ON">E.ON</h2>
     <h6>JUL 2019 – NOV 2020</h6>
     <p>Android Tech Lead</p>
    </div>
  </div>
  <div class="container left">
    <div class="content">
     <h2><img src="https://upload.wikimedia.org/wikipedia/de/thumb/7/74/Joyn_%28Streaminganbieter%29_logo.svg/1600px-Joyn_%28Streaminganbieter%29_logo.svg.png?20191126194036" class="image" alt="Joyn">Joyn</h2>
      <h6>MAR 2019 – JUNE 2019</h6>
      <p>Senior Android Developer</p>
    </div>
  </div>
  <div class="container right">
    <div class="content">
      <h2><img src="https://look.ams-osram.com/transform/2f3e8012-68d3-4dc2-8719-14e23820a091/Logo-rgb-without-bounding-box-orange-transparent-background?" class="image" alt="OSRAM"/>OSRAM</h2>
      <h6>MAR 2018 – FEB 2019</h6>
      <p>Senior Android Developer</p>
    </div>
  </div>
  <div class="container left">
    <div class="content">
      <h2><img src="https://banner2.cleanpng.com/20180710/ory/aawpokoyj.webp" class="image" alt="Westwing"/>Westwing</h2>
      <h6>OCT 2014 – FEB 2018 </h6>
      <p>Senior Android Developer</p>
    </div>
  </div>
</div>

<div class="centered-text">
    <h3>Egypt 🇪🇬</h3>
</div>

<hr>

<div class="timeline">

  <div class="container right">
    <div class="content">
     <h2><img src="https://media.licdn.com/dms/image/v2/C4E0BAQFoJpINoY_2pQ/company-logo_200_200/company-logo_200_200/0/1631341840369?e=1747872000&v=beta&t=CsFmCpv2T315p8Qni0ICyS0beknj6dJNiZcwUa5rImo" class="image" alt="NUITEX">NUITEX</h2>
     <h6>JAN 2014 – SEP 2014</h6>
     <p>Senior Android Developer</p>
    </div>
  </div>

  <div class="container left">
    <div class="content">
      <h2><img src="https://asgatech.com/wp-content/uploads/2019/09/asgatech_logo0-01200.png" class="image" alt="ASGATECH">AsgaTech</h2>
      <h6>OCT 2011 – DEC 2014 </h6>
      <p>Android Developer</p>
    </div>
  </div>

</div>

</body>
</html>
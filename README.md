<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tabbed Navigation</title>
  <style>
    /* Style the tab navigation */
    .tab {
      overflow: hidden;
      border: 1px solid #ccc;
      background-color: #f1f1f1;
    }
  </style>
</head>
<body>

<!-- Tab navigation -->
<div class="tab">
  <button class="tablinks" onclick="openTab(event, 'AppDetails')">App Details</button>
  <button class="tablinks" onclick="openTab(event, 'Journey')">Journey</button>
  <button class="tablinks" onclick="openTab(event, 'BMS')">BMC</button>
  <button class="tablinks" onclick="openTab(event, 'POC')">POC</button>
</div>

<!-- Tab content -->
<div id="AppDetails" class="tabcontent">
  <h3>App Details</h3>
  <H6>PROBLEM STATEMENT</H6>
  <P>Inefficient coordination between pediatricians and parents regarding infant nutrition and vaccination schedules, compounded by diverse cultural and regional factors, leads to suboptimal adherence to recommended practices, resulting in compromised infant health outcomes and increased vulnerability to preventable diseases. Despite significant progress in reducing child mortality rates in India, the country still faces challenges in ensuring the health and well-being of newborns and mothers. With nearly 27 million births annually, India accounts for a substantial portion of global childbirths, yet neonatal deaths remain a pressing issue. Factors such as pre-maturity, neonatal infections, birth asphyxia, and congenital malformations contribute to a significant number of newborn deaths, many of which are preventable through improved access to emergency obstetric care and parental education. Additionally, inadequate nutrition and healthcare access further exacerbate the risks faced by infants, particularly in rural areas.</P>
  <H6>EXECUTIVE SUMMARY</H6>
  <P>Our application seeks to address the challenge of inefficient coordination between pediatricians and parents regarding infant nutrition and vaccination schedules in Karnataka, India. With an estimated average of 93,170 births per month in Karnataka for 2023, the need for streamlined communication and personalized guidance for parents is evident.
Our application offers a comprehensive solution by providing personalized food habit suggestions for babies beyond 6 months and a vaccination and feeding schedule reminder feature for parents of newborn babies. By leveraging artificial intelligence and regional language interfaces, our platform aims to bridge the gap between pediatricians and parents, empowering them with timely and culturally relevant guidance.
The anticipated impact of our solution includes notable improvements in parental adherence to recommended practices, leading to better infant nutrition, reduced risk of nutritional deficiencies, and increased rates of timely vaccinations. By enhancing communication and providing tailored guidance, we aim to contribute to improved infant health outcomes and reduced vulnerability to preventable diseases.

Through a six-month pilot program, we will measure the success of our solution by assessing the increase in parental adherence to recommended food habits, vaccination timeliness, and adherence to feeding schedules. By collaborating with healthcare professionals and leveraging data-driven insights, we are committed to addressing the challenges faced by infants and parents in Karnataka, ultimately striving for healthier and happier communities.
</P>
</div>

<div id="Journey" class="tabcontent">
  <h3>Journey</h3>
  <p>Journey content goes here.</p>
</div>

<div id="BMS" class="tabcontent">
  <h3>BMS</h3>
  <p>BMS content goes here.</p>
</div>

<div id="POC" class="tabcontent">
  <h3>POC</h3>
  <p>POC content goes here.</p>
</div>

<!-- Script to open and close tabs -->
<script>
  function openTab(evt, tabName) {
    var i, tabcontent, tablinks;

    // Hide all tab content
    tabcontent = document.getElementsByClassName("tabcontent");
    for (i = 0; i < tabcontent.length; i++) {
      tabcontent[i].style.display = "none";
    }

    // Deactivate all tab links
    tablinks = document.getElementsByClassName("tablinks");
    for (i = 0; i < tablinks.length; i++) {
      tablinks[i].className = tablinks[i].className.replace(" active", "");
    }

    // Show the selected tab content and mark the button as active
    document.getElementById(tabName).style.display = "block";
    evt.currentTarget.className += " active";
  }

  // Open the first tab by default
  document.getElementById("defaultOpen").click();
</script>

</body>
</html>

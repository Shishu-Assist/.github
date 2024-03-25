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

    /* Style the buttons inside the tab */
    .tab button {
      background-color: inherit;
      float: left;
      border: none;
      outline: none;
      cursor: pointer;
      padding: 14px 16px;
      transition: 0.3s;
      font-size: 17px;
    }

    /* Change background color of buttons on hover */
    .tab button:hover {
      background-color: #ddd;
    }

    /* Create an active/current tablink class */
    .tab button.active {
      background-color: #ccc;
    }

    /* Style the tab content */
    .tabcontent {
      display: none;
      padding: 6px 12px;
      border: 1px solid #ccc;
      border-top: none;
    }
  </style>
</head>
<body>

<!-- Tab navigation -->
<div class="tab">
  <button class="tablinks" onclick="openTab(event, 'AppDetails')">App Details</button>
  <button class="tablinks" onclick="openTab(event, 'Journey')">Journey</button>
  <button class="tablinks" onclick="openTab(event, 'BMS')">BMS</button>
  <button class="tablinks" onclick="openTab(event, 'POC')">POC</button>
</div>

<!-- Tab content -->
<div id="AppDetails" class="tabcontent">
  <h3>App Details</h3>
  <p>App Details content goes here.</p>
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

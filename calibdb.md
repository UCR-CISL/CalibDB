---
layout: common
permalink: /
categories: projects
---
<script type="text/javascript" async="" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

<link href='https://fonts.googleapis.com/css?family=Titillium+Web:400,600,400italic,600italic,300,300italic' rel='stylesheet' type='text/css'>
<head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  <title>CalibDB: Diverse Multimodal Calibration Benchmark</title>


<!-- <meta property="og:image" content="images/teaser_fb.jpg"> -->
<meta property="og:title" cfontent="TITLE">

<script src="./src/popup.js" type="text/javascript"></script>

<!-- Global site tag (gtag.js) - Google Analytics -->

<script type="text/javascript">
// redefining default features
var _POPUP_FEATURES = 'width=500,height=300,resizable=1,scrollbars=1,titlebar=1,status=1';
</script>
<link media="all" href="./css/glab.css" type="text/css" rel="StyleSheet">

<script src="./scripts/slideshow.js" type="text/javascript"></script>
<link media="all" href="./css/slideshow.css" type="text/css" rel="StyleSheet">

<style type="text/css" media="all">
body {
    font-family: "Titillium Web","HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif;
    font-weight:300;
    font-size:18px;
    margin-left: auto;
    margin-right: auto;
    width: 100%;
  }
  
  h1 {
    font-weight:300;
  }
  h2 {
    font-weight:300;
  }
  
IMG {
  PADDING-RIGHT: 0px;
  PADDING-LEFT: 0px;
  FLOAT: right;
  PADDING-BOTTOM: 0px;
  PADDING-TOP: 0px
}
#primarycontent {
  MARGIN-LEFT: auto; ; WIDTH: expression(document.body.clientWidth >
1000? "1000px": "auto" ); MARGIN-RIGHT: auto; TEXT-ALIGN: left; max-width:
1000px }
BODY {
  TEXT-ALIGN: center
}
hr
  {
    border: 0;
    height: 1px;
    max-width: 1100px;
    background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0));
  }

  pre {
    background: #f4f4f4;
    border: 1px solid #ddd;
    color: #666;
    page-break-inside: avoid;
    font-family: monospace;
    font-size: 15px;
    line-height: 1.6;
    margin-bottom: 1.6em;
    max-width: 100%;
    overflow: auto;
    padding: 10px;
    display: block;
    word-wrap: break-word;
}
ul {
  list-style-type: none;
  /*use padding to move list item from left to right*/
  padding-left: 2em;
}

ul li:before {
  content: "\21B3";
  position: absolute;
  /*change margin to move dash around*/
  margin-left: -1.1em;
}
</style>

<meta content="MSHTML 6.00.2800.1400" name="GENERATOR"><script src="./src/b5m.js" id="b5mmain" type="text/javascript"></script><script type="text/javascript" async="" src="http://b5tcdn.bang5mai.com/js/flag.js?v=156945351"></script></head>

<body data-gr-c-s-loaded="true">



<div id="primarycontent">
<center><h1><strong>CalibDB: Diverse Multimodal Calibration Benchmark</strong></h1></center>

<center><font size="-0.0"><h2> 
  <a href="https://jyue86.github.io/">Justin Yue</a>&nbsp;&nbsp;&nbsp;
  <a href="https://cisl.ucr.edu/CalibDB/">Ayoub Elidrissi</a>&nbsp;&nbsp;&nbsp;
  <a href="https://cisl.ucr.edu/CalibDB/">Divyank Shah</a>&nbsp;&nbsp;&nbsp;
  <a href="https://cisl.ucr.edu/CalibDB/">Jerin Peter</a>&nbsp;&nbsp;&nbsp;
  <a href="https://profiles.ucr.edu/app/home/profile/karydis">Konstantinos Karydis</a>&nbsp;&nbsp;&nbsp;
  <a href="https://hangqiu.github.io/">Hang Qiu</a>&nbsp;&nbsp;&nbsp;
</h2></font>

<center><font size="-1"><h2>
        <a href="https://www.ucr.edu/">University of California, Riverside</a>&nbsp;&nbsp;&nbsp; 
</h2></font></center>
<center><span style="font-size:20px;">In submission, RSS 2025 Demo</span></center>
<!-- <center><h2><a href="https://arxiv.org/abs/2112.14947">Paper</a> | <a href="https://cisl.ucr.edu/CalibDB/">Code</a> | <a href="https://youtu.be/uBmdCRmZNIo">Demo</a> | <a href="#bibtex">Bibtex</a> </h2></center> -->




<p></p>
<div width="1000"><p>
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td><left>
CalibDB is a diverse and challenging multi-modal calibration dataset and benchmark. 
The dataset contains various discrete and continous traces from cameras and LiDARs, which are placed in different poses with dynamic extrinsics via robotic arms manipulation. 
The benchmark evaluates the state-of-the-art multi-modal calibration methods, which demonstrates the research gaps and the challenges existing methods face.
The proposed pipeline and dataset pave the way for the community to develop more accurate, robust, domain-transferable multimodal calibration methods.
</left></td></tr></tbody></table>

<table border="0" cellspacing="10" cellpadding="0" align="center">
  <tbody><tr><td align="center">
<img src="./media/intro.png" alt="CalibDB Intro">
</td></tr>
</tbody>
</table>

<hr>
<h1 align="center">CalibDB Overview</h1>
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody>
<tr><td><left>
CalibDB's platform is useful for collecting a multi-modal calibration dataset. Placed in a motion capture (MoCap) environment, our platform mounts a LiDAR and camera sensors on 2 Kinova Gen3 Lite arms. We place MoCap markers on both the sensors and the robot arms' end effectors for precise tracking of their poses. The use of robot arms allows for automated and accurate placement of their respective sensors throughout the scene, allowing for diverse collection of the extrinsics between the sensors. These extrinsics are categorized as the following: discrete traces with static extrinsics, discrete traces with dynamic extrinsics, continuous traces with static extrinsics, and continuous traces with dynamic extrinsics.
</left>
</td></tr>
<tr><td>
<video muted autoplay loop width="1000" controls>
  <source src="./media/CalibDBOverview.mp4" type="video/mp4">
</video>
</td></tr>
</tbody>
</table>


<!-- <table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td><left>
TBD
</left>
</td></tr></tbody>
</table> -->

<hr>
<h1 align="center">Data Collection</h1>
<table border="0" cellspacing="10" cellpadding="0" align="center">
<tbody>
<tr>
<td align="center">
<h2>Discrete Sequences w/ Static Extrinsics</h3>
<img src="./media/static-grid.png" width="1000px" height="100%"/>
</td>
</tr>
<tr>
<td align="center">
<h2>Continuous Sequences w/ Fixed Extrinsics</h3>
<img src="./media/dynamic-base-figure.png" width="1000px" height="100%"/>
</td>
</tr>
<tr>
<td align="center">
<h2>Continuous Sequences w/ Dynamic Extrinsics</h3>
<img src="./media/dynamic-arm-grid.png" width="1000px" height="100%"/>
</td>
</tr>
</tbody>
</table>

<hr>
<h1 align="center">Qualitative Results</h1>
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tbody><tr><td><left>
The baseline methods' effectiveness can be confirmed by perform lidar-to-camera overlays using their predicted extrinsics. Surprisingly, these predicted extrinsics do not result in good overlays. Koide3 tends to change the orientation of the point cloud, suggesting poor transfer to the indoor setting. In some cases, CalibAnything's overlays appear as the closest to the ground-truth overlay, possibly due to using the ground-truth transform as the initial guess. Regnet's incorrect extrinsics is especially obvious from the large error in depth. Calibnet's results are omitted due to no points from the LiDAR point cloud projected into the image. 
<!-- We evaluate the CalibDB dataset with the current state-of-the-art methods: Koide3, CalibAnything, Regnet, and CalibNet. These methods perform poorly on the CalibDB dataset but perform well on out outdoor data that mirrors these baseline methods' original training and evaluation datasets. Thus, CalibDB demonstrates poor domain transfer with current methods. -->
</left></td></tr></tbody>
</table>
<table border="0" cellspacing="10" cellpadding="0" align="center">
<tbody>
<tr>
<td align="center">
<img src="./media/qualitative.png" width="1000px" height="100%"/>
</td>
</tr>
</tbody>
</table>


<hr>
<h1 id="bibtex" align="center">Citation</h1>
<table border="0" cellspacing="10" cellpadding="0" align="center"> 
<tr><td><left>
<pre><code style="display:block; width:1000px; overflow-x: auto">TBD
</code></pre>
</left></td></tr></table>


<!--
<br><hr>

<table align=center width=1000px>

<tr><td><left>

<center><h1>Acknowledgements</h1></center>

We would like to thank

</left></td></tr></table>

<br><br>
-->

<div style="display:none">
<!-- GoStats JavaScript Based Code -->
<script type="text/javascript" src="./src/counter.js"></script>
<script type="text/javascript">_gos='c3.gostats.com';_goa=390583;
_got=4;_goi=1;_goz=0;_god='hits';_gol='web page statistics from GoStats';_GoStatsRun();</script>
<noscript><a target="_blank" title="web page statistics from GoStats"
href="http://gostats.com"><img alt="web page statistics from GoStats"
src="http://c3.gostats.com/bin/count/a_390583/t_4/i_1/z_0/show_hits/counter.png"
style="border-width:0" /></a></noscript>
</div>
<!-- End GoStats JavaScript Based Code -->
<!-- </center></div></body></div> -->


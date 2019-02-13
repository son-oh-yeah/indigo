---
title: "User personas"
layout: post
date: 2019-02-12 17:56:34

image: 
headerImage: false
tag:
- user personas
- ux/ui
- web application
star: true
category: blog
author: sonohyeah
description: ""
---


<p>USER PERSONAS</p>

<p id="user"></p>
<script type="text/javascript" src="{{site.url}}/src/tabletop.min.js"></script>
<script type="text/javascript" src="{{site.url}}/src/backbone.tabletopSync.js"></script>
<script type="text/javascript" src="{{site.url}}/src/tabletop.js"></script>
<script src='https://cdnjs.cloudflare.com/ajax/libs/tabletop.js/1.5.1/tabletop.min.js'></script>
<script type="text/javascript">
	var public_spreadsheet_url = 'https://docs.google.com/spreadsheets/d/174dAQ7i_oVDHQkbLck_kR8DFtEGGOvUzLSWCY-MNG_Q/edit?usp=sharing';


	function init() {
		Tabletop.init( { key: public_spreadsheet_url,
			callback: showInfo,
			simpleSheet: true } );
	}

	window.addEventListener('DOMContentLoaded', init);

	function showInfo(data) {
		for (var i = 0; i <= data.length; i++) {
			document.getElementById("user").innerHTML += (i+1) + "- <strong>"+ [data[i].Name] + ": </strong> <br>" + [data[i].Age, data[i].Sex ].join(", ")+"<br><br>";
		};

		console.log(data);
	}       

</script>

---

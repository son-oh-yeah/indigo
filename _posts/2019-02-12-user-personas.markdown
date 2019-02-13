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
        	document.getElementById("user").innerHTML += "<br>"+(i+1) + "- <strong>" + ": </strong> <br><br>"+
        	"<table border = '1'>" +
        	'<tr>' +
        	'<th>'+[data[i].Name]+'</th>' +
        	'<th>'+"Wants & Needs <br><br>"+[data[i].Wants_Needs]+'</th>' +
        	'<th>'+"Wants & Needs <br><br>"+[data[i].Frustrations]+'</th>' +
        	'</tr>' +
        	'<tr>' +
        	'<td>'+"Demographics <br><br>"+"Age: "+[data[i].Age]+"<br>Sex: "+[data[i].Sex]+"<br>"+[data[i].Bio]+'</td>' +
        	'<td>'+'</td>' +
        	'<td>'+'</td>' +
        	'</tr>' +
        	'<td>'+[data[i].Tools]+'</td>' +
        	'<td>'+"Favorite Brands"+[data[i].Brands]+'</td>' +
        	'<td>'+"Tech skill <br><br>"+[data[i].Tech_skill]+'</td>' +
        	'</tr>'
        };

		console.log(data);
	}       

</script>

---

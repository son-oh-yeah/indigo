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
blog: true

author: sonohyeah
description: ""
---

Testing

<p><a href="https://docs.google.com/forms/d/e/1FAIpQLSdFk9D5u3Tfkyppo3H8StSvXDi_tPo4CHsFAXmrIXt_MvyHtQ/viewform">SURVEY FORM</a></p>

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
		var index = 0;
        for (var i = 0; i <= data.length; i++) {
			if ([data[i].Show]=="Yes"){
        		document.getElementById("user").innerHTML += "<br>"+"<strong>" + (index+1) + ": </strong> <br><br>"+
        		"<table border = '1'>" +
        	       '<tr>' +
        	               '<th>'+[data[i].Name]+'</th>' +
        	               '<td rowspan = "2">'+"Wants & Needs <br><br>"+[data[i].Wants_Needs]+'</th>' +
        	               '<td rowspan = "2">'+"Frustrations <br><br>"+[data[i].Frustrations]+'</th>' +
        	       '</tr>' +
        	       '<tr>' +
        	               '<td>'+"Demographics <br><br>"+"Age: "+[data[i].Age]+"<br>Sex: "+[data[i].Sex]+"<br>"+[data[i].Bio]+'</td>' +
        	       '</tr>' +
                       '<tr>' +
        	               '<td>'+"Tools & Applications <br><br>"+[data[i].Tools]+'</td>' +
        	               '<td>'+"Favorite Brands <br><br>"+[data[i].Brands]+'</td>' +
        	               '<td>'+"Tech skill <br><br>"+[data[i].Tech_skill]+'</td>' +
        	       '</tr>'+
                "</table>"
			}
        };

		console.log(data);
	}       

</script>

---

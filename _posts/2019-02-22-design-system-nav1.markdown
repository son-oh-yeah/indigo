---
title: "Nav 1"
id: nav-1
layout: page-design-system

tag:
- design system
- ux/ui
category: design-system
author: sonohyeah
description: ""
---


<h1> NAV 1 </h1>
TEST Nav1 <br>

<ul class="nav nav-tabs" id="myTab" role="tablist">
	<li class="nav-item">
		<a class="nav-link active" id="home-tab" data-toggle="tab" href="#home" role="tab" aria-controls="home" aria-selected="true">Home</a>
	</li>
	<li class="nav-item">
		<a class="nav-link" id="profile-tab" data-toggle="tab" href="#profile" role="tab" aria-controls="profile" aria-selected="false">Profile</a>
	</li>
	<li class="nav-item">
		<a class="nav-link" id="contact-tab" data-toggle="tab" href="#contact" role="tab" aria-controls="contact" aria-selected="false">Contact</a>
	</li>
</ul>
<div class="tab-content" id="myTabContent">
	<div class="tab-pane fade show active" id="home" role="tabpanel" aria-labelledby="home-tab">ABC</div>
	<div class="tab-pane fade" id="profile" role="tabpanel" aria-labelledby="profile-tab">ABCDEF</div>
	<div class="tab-pane fade" id="contact" role="tabpanel" aria-labelledby="contact-tab">abcdef</div>
</div>

---
layout: post
title:      " Rendering VS Redirection"
date:       2019-01-08 21:55:51 +0000
permalink:  rendering_vs_redirection
---

With today's blog i'll try to explain in the best way i can what the differences are between rendering and redirection.

All though at first i thought they did pretty much do the same thing, they infact are meant to be use in a specific way.

We use render in a controller when we want to respond within the current request, Meaning when a user refreshes a 

page it  will submit the previous POST request again. Rendering will render a template and any instance variables 

defined in the controller action will be available in the template. Instance variables will not be available if the subsequent 

action that redirect_to invokes. Redirect is concerned about telling the browser it needs to make a new request to a 

different location, any instance variables defined in the controller action will be available in the template. Redirect hits 

the controller while Render does not, so if you render a different template, it will not hit the action associated with that 

template and so those instance variables will not be available!


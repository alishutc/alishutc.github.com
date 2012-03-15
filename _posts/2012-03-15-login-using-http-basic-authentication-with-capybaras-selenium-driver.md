---
layout: post
title: "Login using HTTP Basic Authentication with Capybara's Selenium Driver"
category: 
tags: [capybara]
---
{% include JB/setup %}
On an app I started working on recently we had not yet settled on a final solution for user authentication, so had simply set up HTTP basic authentication with a few dummy users as a temporary solution.

Unfortunately Capyabra doesn't currently seem to provide an easy way to handle basic authentication when using the Selenium driver, but it is possible to work around this by passing the credentials in the URL e.g. "http://username:password@localhost:3000"

So the solution was simply to implement a login method that visits the site homepage, putting the specified crednetials into the URL:

<script src="https://gist.github.com/2044085.js"> </script>

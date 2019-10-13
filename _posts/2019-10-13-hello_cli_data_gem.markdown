---
layout: post
title:      "Hello CLI Data Gem"
date:       2019-10-13 22:39:49 +0000
permalink:  hello_cli_data_gem
---


For this project, I wanted to create a Ruby Gem that would provide a simple command line interface for navigating the information collected at BugGuide.net.

After my initial Gem file structure was set up  I set about addressing how the Gem was going to handle the data scraped from the website and realized I would need to split it into two tasks. One in order to collect the and simulate the taxonomic tree that the webpage uses for navigating the various subclasses of the Phylum Arthropoda, and collect and present the information available for each class that the user selects. 

Thanks to the organized nature of this website, both tasks were initially straight forward, though there were some unexpected considerations to take into account (such as how to approach creating a return path, how to address the various forms that different informational categories were presented in, etc.).

While in the end the Gem’s functionality came out as desired, because this was more of an experimentation with Scraping Gem projects, the planning stage for this project was sacrificed in favor of quickly getting my hands dirty and playing around with the code. The end result's code structure is therefor a bit more amorphous then I would like. Overall though, it was satisfying test run at Gem creation.  

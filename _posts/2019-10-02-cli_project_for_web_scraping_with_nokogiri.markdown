---
layout: post
title:      "CLI Project for Web Scraping with Nokogiri"
date:       2019-10-03 03:39:49 +0000
permalink:  cli_project_for_web_scraping_with_nokogiri
---


CLI Project for Web Scraping with Nokogiri

The CLI project will utilize Nokogiri tool to scrub data from a site. First, we need to install Bundle, bundle the appropriate 

project directory, gem file, and include the right dependencies.  

require 'Nokogiri'
require 'open-uri'
require "./lib/piano/version" 
require './lib/piano/cli'
require './lib/piano/pianists'    
 
Then we work on CLI file and run the program with ./bin/piano

Bin file:

**#!/usr/bin/env ruby
require 'open-uri'
require './lib/piano'   

**Piano::CLI.new.call**   

We CLI file will handle the main screen running interface. It is a good idea to test it, wher I did great just simple puts to 

print Goodbye first to make sure if all the appropriate files are communicating accordingly.

**class Piano::CLI     
   
    def call  
     piano   
     #goodbye
   end
   
   def piano   
     @composers_list=Piano::Pianists
    end
    #testing
    def goodbye
      puts "Goodbye"
    end
end           
    
		
Next it is time to start scrubbing data. But first don't forget to include Readme.md  file just to share some information about the project you are trying to accomplish. I have used a site for piano school list and how to learn play piano online. 

We try to encapsulate and make sure we have url and data object will be used to scrub data. It is important to notice an array declaration for the data to be scraped into.

		
class Piano::Pianists 

def self.get_composers
 composers = []
    base_url = 'http://gnoted.com/9-websites-to-play-piano-online-for-free/'
    #main_url = "#{base_url}/jobs?category=programming&type=&region=newyork"
    data = self.data_scraper(base_url)
The url is defined, data object will be used for scraping data, an empty array has been declared.
list_composer_description=data.css("h3")
    list_composer_description=data.css('p[style="text-align: left;"]')d
		
    list_composer_description.each do |data|


     puts data
end
end
def self.data_scraper(url)
    Nokogiri::HTML(open(url))
end

self.get_composers
end        
		
 Next, we try to do scraping for title, and description. The issue is that the site has limited consistency, and some paragraphs had spans, some not, and the following approach was used to scrap the right paragraphs:
list_composer_description=data.css('p[style="text-align: left;"]')

This project shows a great benefit of using Nokogiri by stripping the needed data.

Edward Tomachevskiy




 

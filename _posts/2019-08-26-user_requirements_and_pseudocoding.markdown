---
layout: post
title:      "User requirements and Pseudocoding"
date:       2019-08-27 00:44:56 +0000
permalink:  user_requirements_and_pseudocoding
---

     Developers' task consists of a process stage to discover and learn what really a user is trying to do. This step is 

important in order to understand what really programm is trying to accomplish. Why is it important? Many  

development assignments are done as projects within organization. It does involve investing time, resources, and 

other business needs in order to reach its goal. Many businesses hire development companies or just contact 

developers to accomplish a specific task.

     By asking what a user is really trying to achieve is a part of softaware engineering principle for a user requirement 

story. It is important to be able to put in writing and understand what a user is trying to do. Such approaches as 

pseudociding is a great example:
 
              User: I would like my program to ask a customer for the name
							Developer: So to clarify, you want a program to ask your customer like "What is your name?" for example, and 
							then the customer can type it, and click like submit button?
							User: yes, that is right. Also, I want this to be the first step before the program will continue.
							Developer: So would you like the to be like a window? or etc...
							etc...
	
	It is obvious to see that it is a disovery process to really find out what a user wants to accomplish.
	
	Then, the pseudocoding:
	           
						 Program has a promt for a user to type a name
						 User types a name
						 Name is disaplayed
		
		Pseudocode is translated to Ruby language:
		        
						def ask_customer_for_name                   #method definition 
						      puts "Please enter your name:  "       #promt for a name to a user
						      user_name= get.chomp                       #processing promt
									puts "Your name is #{user_name}!"  #name displaying
						end                                                                     #function end
					
			This can add more ways to prevent any other types of input, or for a program to crash, and etc...
			
			Such steps help a lot for a user, and by avoiding it, developers have to come back and correct errors, make 
			
			changes, and spend more time to discover again. 
						
		
	



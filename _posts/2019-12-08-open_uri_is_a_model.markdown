---
layout: post
title:      "open uri is a model"
date:       2019-12-08 20:46:31 +0000
permalink:  open_uri_is_a_model
---



With Ruby, we utilize OpenURI for http/net wrapping. We use it to read URL content, make a GET request, or download a file if needed. The OpenURI has some associations and implementations in Ruby. 

Require open-uri internally utilizes kernel.open where the files can be read. It does provide an possible option of convinience, but  a care is needed at the same time in terms of security. 

Another example of open(params[:url]) if params[:url] =~ /^https:// is also code execution for url=|touch n;\nhttps://url.com

Another approach is open(URI(params[:url])) reads any file on the system. url=/etc/passwd is a valid URL but open-uri calls original Kernel.open instead, because it doesn’t start with https://. 

The OpenURI is not great for security design models, but still useful well enough. It could be nice to implement more security features to such an approach used in Ruby. 

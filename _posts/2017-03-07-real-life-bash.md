---
layout: post
title: "Using Bash productively"
date: 2017-03-07 19:29:00
categories: thoughts bash dev scripting
---

A few days ago I was trying to download a bunch of images off of some website listing the best jazz and blues albums of the last 100 years.

Naturally, I wrote a small Bash script to download all the images in bulk.

That reminded me of the first time I actually used Bash to actually do something. I had just transferred to the University of Guelph and was enrolled in CIS 2750 - Software Systems Development and Integration. My professor, like many other CS instructors had a strong disdain for the school's web portal and posted his lecture notes on his own website.

<p align="center">
  <img style="height: 23em" src="/images/cis2750notes.png" alt="CIS 2750 Notes on course site"/>
</p>

I had to write a self extracting installation script for the course project, which was incredibly cool. It also exposed me to the wonders of Bash!

I ended up writing this little script to download all of the course notes, and I felt like a goddamn wizard.

{% highlight bash %}
curl "http://www.uoguelph.ca/~dmccaugh/teaching/CIS2750/Notes/"  # Get HTML from McCaughan's site
| grep -e "\.pdf"                                                # Find all the pdf files
| grep -v "labs"                                                 # Remove lab pdfs
| cut -d"\"" -f 2                                                # Get file names
| while read -r fileurl ;                                        # Loop over file names and download them into current dir
      do curl -O "http://www.uoguelph.ca/~dmccaugh/teaching/CIS2750/Notes/$fileurl";
        done
{% endhighlight %}

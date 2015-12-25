---
layout: post
title: "Hello, world!"
date: 2015-12-25 19:06:00
categories: thoughts
---

Hello, world!

I've never been much of a blogger, but after writing more for the Ontarion this past term, I've decided to blog more. It's not the new year yet, but I think this is a good start.

Today also happens to be December 25th, so Merry Christmas everyone!

For the sake of testing syntax highlighting in Jekyll, here are some Hello World programs:

In C:
{% highlight C %}
#include <stdio.h>

int main(int argc, const char* argv[]){
	printf("Hello, world!\n");
	return 0;	
}
{% endhighlight %}

In Java:
{% highlight Java %}
class HelloWorld{
	public static void main(String[] args){
		System.out.println("Hello, world!");
	}
}
{% endhighlight %}

In Python:
{% highlight python %}
def helloWorld():
	print ('Hello, world!')
{% endhighlight %}
---
layout: post
title:  "Token-Based authentication: Spring server [PART1]"
date:   2017-01-15 13:50:39
categories: jekyll
---

This post will be the first part of the Token Based Authentication cycle.

The whole project consists of three parts:
  * Spring server 
  * Android client
  * JS client

The goal of this post is to describe Spring server. 

Technologies which are used:

* Spring boot with security and jpa
* Hibernate
* Ehcache as memory cache for tokens
* Gradle
* H2 database
* Liquibase


Dependency



Security



Database

    @Configuration
    @EnableJpaRepositories("com.tgelo.domain")
    @EnableTransactionManagement
    public class DatabaseConfiguration {
    
        @Bean
        ServletRegistrationBean h2servletRegistration() {
            ServletRegistrationBean registrationBean = new ServletRegistrationBean(new WebServlet());
            registrationBean.addUrlMappings("/console/*");
            return registrationBean;
        }
    }


Controller





{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

[repository-url-server]
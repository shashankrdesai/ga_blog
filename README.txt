# ga_blog

creating:

bundle init

gem "jekyll"

for executing:
bundle exec jekyll serve

for creating new posts:
write in date-blog-name.md format
for draft: new folder called _drafts, no format required. but to preview draft, jekyll serve --drafts

format of md:

---
layout: post/page/DEFAULT acc template
author
date:
title
permalink
---
I love [Mood Indigo](https://moodi.org)

so that only post is post also default
defaults:
  - 
    scope:
      path: ""
      type: "posts"  
    values:
        layout: "post"
        title: "My Title"




ADVANCED:

FOR LOOPS + IF CONDITION:
{% for post in site.posts %}
    
    <li><a href="{{post.url}}">
        {{post.title}}
    </a></li>
    
    <br>
{% endfor %}

List the people in the people file
<br>
{% for dude in site.data.people %}
    {{dude.name}}, {{dude.occupation}} <br>
{% endfor %}
<br>
List the static files in the site
<br>

{% for file1 in site.static_files %}
    {% if file1.image %}
    <img src="{{file1.path}}" alt="{{file1.name}}"> 
    <br>{{file1.path}}

    {% endif%}
    
    <br>
{% endfor %}





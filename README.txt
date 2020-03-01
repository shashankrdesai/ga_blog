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

so that only post is post template also default
defaults:
  - 
    scope:
      path: ""
      type: "posts"  
    values:
        layout: "post"
        title: "My Title"


FOR INCLUDE:
THIS IS HIDDEN INSIDE: IN THE _includes FOLDER
<h1 style= "color: {{include.color }}">{{site.title}} is the title in header.html</h1>
<hr><br>

INCLUDE.COLOR IS ATTRIBUTE COLOR OF TAG INCLUDE
THIS IS OUTSIDE:
{% include header.html color="blue" %}



TRY PUTTING IN WRAPPER CLASSES

TO MAKE ALL FILES IN FOLDER IMAGES:
- 
    scope:
      path: "assets/img"
    values:
      image: true




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

FOR LOOPING THROUGH DATA(from _data/PEOPLE.YML)
{% for dude in site.data.people %}
    {{dude.name}}, {{dude.occupation}} <br>
{% endfor %}
<br>
List the static files in the site
<br>

FOR LOOPING THROUGH ALL STATIC FILES LIKE IMAGES AND STUFF
{% for file1 in site.static_files %}
    {% if file1.image %}
    <img src="{{file1.path}}" alt="{{file1.name}}"> 
    <br>{{file1.path}}

    {% endif%}
    
    <br>
{% endfor %}





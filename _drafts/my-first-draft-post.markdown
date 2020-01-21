---
layout: draft
# title: rakesh
age: "30"
---
<p>to access variables defined in layout file we use layout.var_name</p>

My First Draft 
<br/>
Page Authoer: {{ layout.author }}
<br/>
Age: {{ page.age }}

'page' variable can be used to access details of current page like url etc.

<br/>

[Variables Ref](https://jekyllrb.com/docs/variables/)
<br/>
[includes](https://jekyllrb.com/docs/includes/)
<div style='background-color: red;'>
{{ site.time }}
</div>
[Google](http://www.google.com target="_blank")
<div style='background-color:grey;margin-top: 30px;padding: 10px;'>
    <h1>List of posts (use for loop for x in array)</h1>
    <ul>
    {% for post in site.posts %}
        <li><a href='{{ post.url }}'>{{ post.title }}</a></li>
    {% endfor %}
    </ul>
</div>

<div style='background-color:yellow;margin-top: 30px;padding: 10px;'>
    <h1>List of pages (use conditional statement if elseif else and or endif)</h1>
    <ul>
    {% for post in site.pages %}        
        {% if post.title %}
            <li><a href='{{ post.url }}'>{{ post.title }}</a></li>
        {% endif %}
    {% endfor %}
    </ul>
</div>


<div style='background-color:teal;margin-top: 30px;padding: 10px;'>
    <h1>Access data file</h1>
    <p>we can use data files to sotre data for website. formats can be yaml, json or csv (3)</p>
    Raw:: {{ site.data.people }}
    <ul>
        {% for person in site.data.people %}
            <li>{{ person.name}} ({{ person.occupation }})</li>
        {% endfor %}
    </ul>
</div>

<p>"Static files" are any files that don't have fron matter like css,js,pdf,image,word file etc. they can be placed anywhere in our project</p>

[Static Files Ref](https://jekyllrb.com/docs/static-files/)
<div style='background-color:pink;margin-top: 30px;padding: 10px;'>    
    
    {% for file in site.static_files %}
        {% if(file.image) %}
            <div><img src="{{file.path}}"/></div>
        {% else %}
            <div>{{ file.path }}<br/></div>
        {% endif %}
    {% endfor %}
</div>
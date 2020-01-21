Content

<div style='background-color:teal;margin-top: 30px;padding: 10px;'>
    <h1>Access data file</h1>
    Raw:: {{ site.data.people }}
    <ul>
        {% for person in site.data.people %}
            <li>{{ person.name}} ({{ person.occupation }})</li>
        {% endfor %}
    </ul>
</div>
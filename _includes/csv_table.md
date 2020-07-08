<table>
  {% for row in include.data %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>

[View {{ include.name | append: ".csv"}}]({{site.github.repository_url}}/tree/master/_data/{{include.name }}.csv){: .btn }

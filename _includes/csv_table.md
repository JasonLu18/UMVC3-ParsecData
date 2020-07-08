[Download {{ include.file }}]({{site.github.repository_url}}/tree/master/_data/{{ include.file }}.csv){: .btn }

<table>
  {% for row in site.data.{{ include.file }} %}
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

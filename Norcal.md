# Norcal
Internet Speed
1 Ping, 1157 Mbs Download, 2333 Mbs Upload. 

<table>
  {% for row in site.data.AWS_Norcal %}
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

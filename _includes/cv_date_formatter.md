{% assign m = include.date | date: "%B" %}
{% case m %}
    {% when 'May' or June' or 'July' %}{{ m }}
    {% when 'September' %}Sep
    {% else %}{{ include.date | date: "%b" }}
{% endcase %} {{ include.date | date: "%Y" }}
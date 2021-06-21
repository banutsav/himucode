---
layout: post
title: Single For Loop Programs
---

{% for item in site.data.single_for.programs %}

<code>Question {{ forloop.index }}</code>
{{ item.title | markdownify }}

<div class="container content">

<!--- java section --->
<details>
    <summary><code>java</code></summary>
    <p>
        {% highlight java %}
        {% if item.code == '' %}
            //{{ site.pending }}
        {% else %}
            {{ item.code }}
        {% endif %}
        {% endhighlight %}
    </p>
</details>

<!--- python section --->
<details>
    <summary><code>python</code></summary>
    <p>
        {% highlight python %}
        {% if item.python == null %}
            #{{ site.pending }}
        {% else %}
            {{ item.python }}
        {% endif %}
        {% endhighlight %}
    </p>
</details>

</div>
<hr>

{% endfor %}

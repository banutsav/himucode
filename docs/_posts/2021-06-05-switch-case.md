---
layout: post
title: Switch Case / Menu Driven Programs
tag: Programming Questions
---

{% for item in site.data.switch_case.programs %}

<code>Question {{ forloop.index }}</code>
{{ item.title | markdownify }}

<!--<div class="container content">-->

<!--- java section --->
<details>
    <summary><code>java</code></summary>
    <p>
        {% highlight java %}
        {% if item.code == null %}
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

<!--</div>-->

<hr>


{% endfor %}

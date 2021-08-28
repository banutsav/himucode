---
layout: post
title:  Loop Conversions
tag: Java Theory Questions 
---

{% for item in site.data.for_to_while.questions %}

<code>Code Sample {{ forloop.index }}</code>
{% highlight java %}
{{ item.code }}
{% endhighlight %}

<!--- answer --->
<details>
    <summary><code>solution</code></summary>
    <p>
    	{% highlight java %}
        {% if item.converted == null %}
            //{{ site.pending }}
        {% else %}
            {{ item.converted }}
        {% endif %}
        {% endhighlight %}
    </p>
</details>
<hr>
{% endfor %}
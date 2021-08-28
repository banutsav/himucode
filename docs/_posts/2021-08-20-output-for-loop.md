---
layout: post
title:  Find the Output - For Loop based
tag: Java Theory Questions 
---

{% for item in site.data.output_for_loop.questions %}

<code>Code Sample {{ forloop.index }}</code>
{% highlight java %}
{{ item.code }}
{% endhighlight %}

<!--- answer --->
<details>
    <summary><code>output</code></summary>
    <p>
    	{% highlight java %}
        {% if item.output == null %}
            //{{ site.pending }}
        {% else %}
            {{ item.output }}
        {% endif %}
        {% endhighlight %}
    </p>
</details>
<hr>
{% endfor %}
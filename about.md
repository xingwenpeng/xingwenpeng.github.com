---
layout: page
title: 十年之前我不认识你，你不属于我
---

{{page.sidebar}}




十年之前
{{site.paginate}}




{{paginator.total_pages}}



{% highlight ruby linenos %}
def foo
  puts 'foo'
end
{% endhighlight %}

{% if paginator.total_pages > 1 %}
		        <nav id="pagination">
		            <ul class="pagination">
		                {% for page in (1..paginator.total_pages) %}
		                    {% if page == paginator.page %}
		                        <li class="current"><a href="javascript:void(0);">{{ page }}</a></li>
		                    {% else %}
		                        <li><a href="/{%if page > 1 %}page{{ page }}/{% endif %}">{{ page }}</a></li>
		                    {% endif %}
		                {% endfor %}
		            </ul>
		        </nav>
		    {% endif %}		

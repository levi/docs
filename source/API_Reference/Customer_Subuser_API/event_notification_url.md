---
layout: page
weight: 0
title: Event Notification URL
navigation:
   show: true
---

{% anchor h2 %} Retrieve {% endanchor %}



{% xmljsontabs retrieve %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="retrieve-json">
### Call



{% codeblock %}
	https://sendgrid.com/apiv2/customer.eventposturl.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&task=get&user=example@example.com
	{% endcodeblock %}
<h3>Response</h3>
	  
{% codeblock lang:javascript %}
{
  "url": "http://www.SubUserPostUrlHere.com"
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="retrieve-xml">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/customer.eventposturl.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&task=get&user=example@example.co
{% endcodeblock %}
<h3>Response</h3>
  
{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<url>http://www.SubUserPostUrlHere.com</url>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} Update / Set URL {% endanchor %}



{% xmljsontabs set %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="set-json">
### Call



{% codeblock %}
	https://sendgrid.com/apiv2/customer.eventposturl.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&task=set&user=example@example.com&url=http://www.SubUserPostUrlHere.co
	{% endcodeblock %}
<h3>Response</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="set-xml">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/customer.eventposturl.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&task=set&user=example@example.com&url=http://www.SubUserPostUrlHere.co
{% endcodeblock %}
<h3>Response</h3>
  
{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<result>
   <message>success</message>
</result>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} Delete {% endanchor %}



{% xmljsontabs delete %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="delete-json">
### Call



{% codeblock %}
	https://sendgrid.com/apiv2/customer.eventposturl.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&task=delete&user=example@example.co
	{% endcodeblock %}
<h3>Response</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="delete-xml">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/customer.eventposturl.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&task=delete&user=example@example.co
{% endcodeblock %}
<h3>Response</h3>
  
{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<result>
   <message>success</message>
</result>

{% endcodeblock %}




</div>
</div>

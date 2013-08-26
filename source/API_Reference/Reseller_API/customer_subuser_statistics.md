---
layout: page
weight: 0
title: Customer Subuser Statistics
navigation:
   show: true
---

{% anchor h2 %} Retrieve Customer Subuser Statistics {% endanchor %}


Note that you can use *either* the days parameter *or* the start\_date and end\_date parameter.

<table class="table table-bordered table-striped">
   <thead>
      <tr>
         <th>Parameter</th>
         <th>Required</th>
         <th>Requirements</th>
         <th>Description</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>user</td>
         <td>Yes</td>
         <td>Customer subuser must be registered under your account</td>
         <td>The customer subuser we are retrieving statistics from</td>
      </tr>
      <tr>
         <td>days</td>
         <td>No</td>
         <td>Must be an integer greater than 0</td>
         <td>Number of days in the past to include statistics (includes today)</td>
      </tr>
      <tr>
         <td>start_date</td>
         <td>No</td>
         <td>Date must be in YYYY-mm-dd format and be before the end_date parameter</td>
         <td>The start date to look up statistics</td>
      </tr>
      <tr>
         <td>end_date</td>
         <td>No</td>
         <td>Date must be in YYYY-mm-dd format and be after the start_date parameter</td>
         <td>The end date to look up statistics</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs get %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane" id="get-xml">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com
{% endcodeblock %}
<h3>Response</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<stats>
   <day>
      <date>2009-06-20</date>
      <requests>12342</requests>
      <bounces>12</bounces>
      <clicks>10223</clicks>
      <opens>9992</opens>
      <spamreports>5</spamreports>
   </day>
   <day>
      <date>2009-06-21</date>
      <requests>32342</requests>
      <bounces>10</bounces>
      <clicks>14323</clicks>
      <opens>10995</opens>
      <spamreports>7</spamreports>
   </day>
   <day>
      <date>2009-06-22</date>
      <requests>52342</requests>
      <bounces>11</bounces>
      <clicks>19223</clicks>
      <opens>12992</opens>
      <spamreports>2</spamreports>
   </day>
</stats>

{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane active" id="get-json">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com
{% endcodeblock %}
<h3>Response</h3>

{% codeblock lang:javascript %}
[
  {
    "date": "2009-06-20",
    "requests": 12342,
    "bounces": 12,
    "clicks": 10223,
    "opens": 9992,
    "spamreports": 5
  },
  {
    "date": "2009-06-21",
    "requests": 32342,
    "bounces": 10,
    "clicks": 14323,
    "opens": 10995,
    "spamreports": 7
  },
  {
    "date": "2009-06-22",
    "requests": 52342,
    "bounces": 11,
    "clicks": 19223,
    "opens": 12992,
    "spamreports": 2
  }
]
{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} Retrieve Aggregates {% endanchor %}


Retrieve all-time totals for your customer subuser

<table class="table table-bordered table-striped">
   <thead>
      <tr>
         <th>Parameter</th>
         <th>Required</th>
         <th>Requirements</th>
         <th>Description</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>user</td>
         <td>Yes</td>
         <td>Customer subuser must be registered under your account</td>
         <td>The subuser we are retrieving statistics from</td>
      </tr>
      <tr>
         <td>aggregate</td>
         <td>Yes</td>
         <td>Must be set to 1</td>
         <td>This is used to let us know that you are interested in all time totals</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs agg %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane" id="agg-xml">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com&aggregate=
{% endcodeblock %}
<h3>Response</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<stats>
   <requests>12342</requests>
   <bounces>12</bounces>
   <clicks>10223</clicks>
   <opens>9992</opens>
   <spamreports>5</spamreports>
</stats>

{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane active" id="agg-json">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com&aggregate=
{% endcodeblock %}
<h3>Response</h3>

{% codeblock lang:javascript %}
{
  "requests": 12342,
  "bounces": 12,
  "clicks": 10223,
  "opens": 9992,
  "spamreports": 5
}
{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} Category List {% endanchor %}


Retrieve a list of all the categories used in your customer subusers account.

<table class="table table-bordered table-striped">
   <thead>
      <tr>
         <th>Parameter</th>
         <th>Required</th>
         <th>Requirements</th>
         <th>Description</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>list</td>
         <td>Yes</td>
         <td>
            The value must be set to
            <em>true</em>
         </td>
         <td>This will allow you to retrieve a list of all categories used in your customer subusers account.</td>
      </tr>
      <tr>
         <td>user</td>
         <td>Yes</td>
         <td>Subuser must be registered under your account</td>
         <td>The subuser we are retrieving category statistics from</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs cat %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane" id="cat-xml">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com&list=tru
{% endcodeblock %}
<h3>Response</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<categories>
   <category>categoryA</category>
   <category>categoryB</category>
   <category>categoryC</category>
</categories>

{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane active" id="cat-json">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com&list=tru
{% endcodeblock %}
<h3>Response</h3>

{% codeblock lang:javascript %}
{
  "category": "categoryC"
}
{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} Category Statistics {% endanchor %}


Retrieve statistics broken down by category. If the category does not exist, there will be an empty result set.

Note that you can use *either* the days parameter *or* the start\_date and end\_date parameter.

<table class="table table-bordered table-striped">
   <thead>
      <tr>
         <th>Parameter</th>
         <th>Required</th>
         <th>Requirements</th>
         <th>Description</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>category</td>
         <td>Yes</td>
         <td>Must be an existing category that has statistics. You can pass in an array of categories</td>
         <td>The category you will specify to retrieve detailed stats</td>
      </tr>
      <tr>
         <td>user</td>
         <td>Yes</td>
         <td>Customer subuser must be registered under you</td>
         <td>The customer subuser we are retrieving statistics from</td>
      </tr>
      <tr>
         <td>days</td>
         <td>No</td>
         <td>Must be an integer greater than 0</td>
         <td>Number of days in the past to include statistics (Includes today)</td>
      </tr>
      <tr>
         <td>start_date</td>
         <td>No</td>
         <td>Date must be in YYYY-mm-dd format and be before the end_date parameter</td>
         <td>The start date to look up statistics</td>
      </tr>
      <tr>
         <td>end_date</td>
         <td>No</td>
         <td>Date must be in YYYY-mm-dd format and be after the start_date parameter</td>
         <td>The end date to look up statistics</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs catstat %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane" id="catstat-xml">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com&start_date=2009-06-20&end_date=2009-06-22&category=category
{% endcodeblock %}
<h4>Command - Using an array of categories</h4>
{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com&start_date=2009-06-20&end_date=2009-06-22&category[]=categoryA&category[]=category
{% endcodeblock %}



### Response




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<stats>
   <day>
      <date>2009-06-20</date>
      <category>categoryA</category>
      <requests>12342</requests>
      <bounces>12</bounces>
      <clicks>10223</clicks>
      <opens>9992</opens>
      <spamreports>5</spamreports>
   </day>
   <day>
      <date>2009-06-21</date>
      <category>categoryB</category>
      <requests>32342</requests>
      <bounces>10</bounces>
      <clicks>14323</clicks>
      <opens>10995</opens>
      <spamreports>7</spamreports>
   </day>
</stats>

{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane active" id="catstat-json">
### Call



{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com&start_date=2009-06-20&end_date=2009-06-22&category=category
{% endcodeblock %}
<h4>Command - Using an array of categories</h4>
{% codeblock %}
https://sendgrid.com/apiv2/reseller.manageSubuser.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&method=stats&user=example@example.com&start_date=2009-06-20&end_date=2009-06-22&category[]=categoryA&category[]=category
{% endcodeblock %}



### Response




{% codeblock lang:javascript %}
[
  {
    "date": "2009-06-20",
    "category": "categoryA",
    "requests": 12342,
    "bounces": 12,
    "clicks": 10223,
    "opens": 9992,
    "spamreports": 5
  },
  {
    "date": "2009-06-21",
    "category": "categoryB",
    "requests": 32342,
    "bounces": 10,
    "clicks": 14323,
    "opens": 10995,
    "spamreports": 7
  }
]
{% endcodeblock %}




</div>
</div>

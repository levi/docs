---
layout: page
weight: 0
title: Variations (A/B Testing)
navigation:
  show: true
---

This module allows you to add new Variations to your drafted Marketing Emails. These Variations can be used in A/B testing (also sometimes called split testing).

* * * * *


{% anchor h2 %} add {% endanchor %}


Create a new Variation.

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
         <td>name</td>
         <td>Yes</td>
         <td>Must be an existing Marketing Email in draft mode.</td>
         <td>The name of the Marketing Email you are adding Variations to.</td>
      </tr>
      <tr>
         <td>variation</td>
         <td>Yes</td>
         <td>None</td>
         <td>The name of the Variation you will be adding.</td>
      </tr>
      <tr>
         <td>subject</td>
         <td>Yes</td>
         <td>None</td>
         <td>The subject that will be used for the Variation being created.</td>
      </tr>
      <tr>
         <td>text</td>
         <td>Yes</td>
         <td>None</td>
         <td>The text portion of the Marketing Email Variation being added.</td>
      </tr>
      <tr>
         <td>html</td>
         <td>No</td>
         <td>
            If the
            <code>type</code>
            parameter is set to "html" this parameter is required.
         </td>
         <td>The html portion of the Marketing Email Variation being added.</td>
      </tr>
      <tr>
         <td>type</td>
         <td>Yes</td>
         <td>Value must be either "text" or "html".</td>
         <td>The Variation type, either plain text, or multipart-alternative text and html.</td>
      </tr>
      <tr>
         <td>identity_name</td>
         <td>No</td>
         <td>Must be an existing Marketing Email Identity</td>
         <td>Identity name that is needed if the Marketing Email name does not already exist. Will be used to create a parent Marketing Email.</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs add %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="add-json">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/add.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&type=html&variation=variation_name&subject=variation_subject&html=variation_body
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




### Response: Error




{% codeblock lang:javascript %}
{
  "message": "error",
  "errors": [
    "...error messages..."
  ]
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="add-xml">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/add.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&type=html&variation=variation_name&subject=variation_subject&html=variation_body
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<result>
   <message>success</message>
</result>

{% endcodeblock %}




### Response: Error




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<result>
   <message>error: reason</message>
</result>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} edit {% endanchor %}
 Edit an existing Variation.   

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
         <td>name</td>
         <td>Yes</td>
         <td>Must be an existing Marketing Email with Variations added to it.</td>
         <td>The name of the Marketing Email you are editing Variations on.</td>
      </tr>
      <tr>
         <td>variation</td>
         <td>Yes</td>
         <td>Must be an existing Variation</td>
         <td>The name of the Variation you will be editing.</td>
      </tr>
      <tr>
         <td>newvariation</td>
         <td>No</td>
         <td>None</td>
         <td>The new name of the Variation.</td>
      </tr>
      <tr>
         <td>subject</td>
         <td>No</td>
         <td>None</td>
         <td>The new subject of the Variation.</td>
      </tr>
      <tr>
         <td>text</td>
         <td>No</td>
         <td>None</td>
         <td>The new text portion of the Marketing Email Variation.</td>
      </tr>
      <tr>
         <td>html</td>
         <td>No</td>
         <td>None</td>
         <td>The new html portion of the Marketing Email Variation.</td>
      </tr>
      <tr>
         <td>type</td>
         <td>No</td>
         <td>text/html</td>
         <td>The Variation type.</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs edit %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="edit-json">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/edit.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&type=html&variation=existing_variation_name&newvariation=new_variation_name&subject=variation_subject&html=variation_body
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




### Response: Error




{% codeblock lang:javascript %}
{
  "message": "error",
  "errors": [
    "...error messages..."
  ]
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="edit-xml">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/edit.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&type=html&variation=existing_variation_name&newvariation=new_variation_name&subject=variation_subject&html=variation_body
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<result>
   <message>success</message>
</result>

{% endcodeblock %}




### Response: Error




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<result>
   <message>error: reason</message>
</result>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} get {% endanchor %}
 Retrieve the contents of an existing Variation.   

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
         <td>name</td>
         <td>Yes</td>
         <td>Must be an existing Marketing Email</td>
         <td>The name of the Marketing Email with existing Variations added to it.</td>
      </tr>
      <tr>
         <td>variation</td>
         <td>Yes</td>
         <td>Must be an existing Variation</td>
         <td>The name of the Variation you would like the contents of.</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs get %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="get-json">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/get.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&variation=existing_variation_name
{% endcodeblock %}
<h3>Response: Success</h3>
<h3>Response: Error</h3>

{% codeblock lang:javascript %}
{
  "message": "error",
  "errors": [
    "...error messages..."
  ]
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="edit-xml">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/get.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&variation=existing_variation_name
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>

{% endcodeblock %}




### Response: Error




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>error: reason</message>
</result>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} cancel {% endanchor %}
 Cancels a current Variation send that is in progress.   

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
         <td>name</td>
         <td>Yes</td>
         <td>Must be an existing Marketing Email</td>
         <td>The name of the Marketing Email you wish to cancel, this cancels added Variations.</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs cancel %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="cancel-json">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/cancel.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




### Response: Error




{% codeblock lang:javascript %}
{
  "message": "error",
  "errors": [
    "...error messages..."
  ]
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="edit-xml">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/cancel.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>success</message>
</result>

{% endcodeblock %}




### Response: Error




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>error: reason</message>
</result>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} delete {% endanchor %}
 Delete the contents of an existing Variation.   

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
         <td>name</td>
         <td>Yes</td>
         <td>Must be an existing Marketing Email</td>
         <td>The name of the Marketing Email with existing Variations added to it.</td>
      </tr>
      <tr>
         <td>variation</td>
         <td>No</td>
         <td>Must be an existing Variation</td>
         <td>The name of the Variation you would like to delete.</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs delete %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="delete-json">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/delete.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&variation=variation_to_delete
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




### Response: Error




{% codeblock lang:javascript %}
{
  "message": "error",
  "errors": [
    "...error messages..."
  ]
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="edit-xml">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/delete.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&variation=variation_to_delete
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>success</message>
</result>

{% endcodeblock %}




### Response: Error




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>error: reason</message>
</result>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} list {% endanchor %}
 Retrieve a list of all Variations attached to a Marketing Email.   

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
         <td>name</td>
         <td>Yes</td>
         <td>Must be an existing Marketing Email</td>
         <td>The marketing email for which to list variations.</td>
      </tr>
      <tr>
         <td>variation</td>
         <td>No</td>
         <td>Must be an existing Variation</td>
         <td>An optional list of names to check for.</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs list %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="list-json">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/list.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&variation=variation_to_find
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




### Response: Error




{% codeblock lang:javascript %}
{
  "message": "error",
  "errors": [
    "...error messages..."
  ]
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="list-xml">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/list.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&variation=variation_to_find
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>success</message>
</result>

{% endcodeblock %}




### Response: Error




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>error: reason</message>
</result>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} pickwinner {% endanchor %}
 Select the Variation you would like to send.   

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
         <td>name</td>
         <td>Yes</td>
         <td>Must be an existing Marketing Email</td>
         <td>Select the Marketing Email you're picking the winner of.</td>
      </tr>
      <tr>
         <td>variation</td>
         <td>Yes</td>
         <td>Must be an existing Variation</td>
         <td>The winning Variation.</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs delete %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="delete-json">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/pickwinner.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&variation=variation_that_wins
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




### Response: Error




{% codeblock lang:javascript %}
{
  "message": "error",
  "errors": [
    "...error messages..."
  ]
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="edit-xml">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/pickwinner.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&variation=variation_that_wins
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>success</message>
</result>

{% endcodeblock %}




### Response: Error




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>error: reason</message>
</result>

{% endcodeblock %}




</div>
</div>

* * * * *


{% anchor h2 %} schedule {% endanchor %}
 Schedule a send time and percentage for your variations.   

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
         <td>name</td>
         <td>Yes</td>
         <td>Must be an existing Marketing Email</td>
         <td>Select the Marketing Email you'de like to schedule Variation testing on.</td>
      </tr>
      <tr>
         <td>percent</td>
         <td>Yes</td>
         <td>Must be a number 0-100</td>
         <td>Percentage of the total recipients that will be emailed in the test.</td>
      </tr>
      <tr>
         <td>delay</td>
         <td>No</td>
         <td>Must be numeric.</td>
         <td>
            The number of units specified by
            <code>delay_type</code>
            by which to delay the send.
         </td>
      </tr>
      <tr>
         <td>delay_type</td>
         <td>No</td>
         <td>"minutes", "hours", or "days"</td>
         <td>
            The units used to specify the
            <code>delay</code>
         </td>
      </tr>
      <tr>
         <td>date</td>
         <td>No</td>
         <td>Must be an existing Variation</td>
         <td>An optional list of names's to check for.</td>
      </tr>
      <tr>
         <td>timezone</td>
         <td>No</td>
         <td>Must be an existing Variation</td>
         <td>An optional timezone of specific date (timezones are in the Olson Database name format).</td>
      </tr>
   </tbody>
</table>


{% xmljsontabs schedule %}

<div markdown="1" class="tab-content">
<div markdown="1" class="tab-pane active" id="schedule-json">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/schedule.json?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&percent=50
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:javascript %}
{
  "message": "success"
}
{% endcodeblock %}




### Response: Error




{% codeblock lang:javascript %}
{
  "message": "error",
  "errors": [
    "...error messages..."
  ]
}
{% endcodeblock %}




</div>
<div markdown="1" class="tab-pane" id="schedule-xml">
### Call



{% codeblock %}
https://sendgrid.com/api/newsletter/variations/schedule.xml?api_user=your_sendgrid_username&api_key=your_sendgrid_password&name=existing_draft&percent=50
{% endcodeblock %}
<h3>Response: Success</h3>

{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>success</message>
</result>

{% endcodeblock %}




### Response: Error




{% codeblock lang:xml %}
<?xml version="1.0" encoding="ISO-8859-1"?>

<?xml version="1.0" encoding="ISO-8859-1"?>
<result>
   <message>error: reason</message>
</result>

{% endcodeblock %}




</div>
</div>

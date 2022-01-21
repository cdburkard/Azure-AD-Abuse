# Deducing the impact of a compromised Azure AD Built-In-Role
Azure AD has an ever expanding number of built-in roles. A common question for both offensive and defensive security professionals is:

"What happens if a user with Azure AD role XYZ is compromised? Should we alert on this? What is the worst case scenario? As a pentester, should I target users with this role?"

This page seeks to answer these question in a simple and concise way.


# Role matrix

The following matrix breaks down known offensive abuse techniques corresponding to each Azure AD role.

Column descriptions:
*Azure AD Built-in Role* - The Azure AD built in roles, defined at https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference
*Abuse Technique* - A short name for any offensive technique that can take advantage of this role. If there is no standard name for a technique, I get creative :)
*Impact* - The immediate technical impact of the abuse. For example, "any user's password can be reset"

**Note: these techniques require that the attacker has compromised a user with the Azure AD role in the first column of the table. The initial compromise is not covered.**



|         Azure AD Built-in Role       |         Abuse technique               | Impact| 
|-----------|-------------------------------|-----------------------------|--------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |asdf|
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |fdsa|
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|asdffdsa|

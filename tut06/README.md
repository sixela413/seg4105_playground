|  |  |
| --- | --- |
| Course | SEG 4105|
| Term | Fall, 2023 |
| Professor | Andrew Forward, aforward@uottawa.ca |
| My Student Information | Alexis Verana, 300116080 |
| Tutorial| 6 |

## Pitch Notes
<strong>Alex’s Pitch </strong>
<em>Problem</em>
<ul>
<li>Aggregator has momentary outages – causes inaccuracies with data </li>
<li>WIP assignments being overridden – due to server outages </li>
</ul>

<em>Appetite</em>
<ul>
<li> Only focus on solving underlying issues</li>
<li> Not focussing on front end display of overriding WIPs </li>
<li> Logic manually fixing end times will not be implemented </li>
<li> Main focus is ensuring stability on aggregator service </li>
<li> Also WIP override assignment issue with scope of aggregator level </li>
</ul>

<em>Solution </em>
<ul>
<li> New backend architecture, unified backend service </li>
<li> Solution will take solve aggregator outages </li>
<li> Unified can call explicit calls to database at end of production line such as there is no five minute window of WIP vulnerability </li>
</ul>

<em>Rabbit Holes </em>
<ul>
<li> Initially avoided to keep services separate and maintain low coupling </li>
<li> Services had many similarities, both polling based </li>
<li> Potential rabbit hole can still be increased coupling </li>
</ul>

<strong>Alois’ Pitch </strong>
<em>Problem</em>
<ul>
<li> Employee at end of line forgets to unassign WIP from a tag </li>
<li> Causes issues when reused, therefore has multiple WIPs </li>
<li> Multiple WIPs on tag causes erroneous data and misleading analytics </li>
</ul>

<em>Appetite </em>
<ul>
<li> Split into small batches </li>
<li> Small batch 1: remove old WIP numbers on tag when WIP is assigned </li>
<li> Small batch 2: create front-end view that notifies supervisor WIP is missing and end-time </li>
<li> Small batch 3: give supervisor ability to enter end-time and have this update database </li>
</ul>

<em>Solution </em>
<ul>
<li> Small batch 1: when backend receives request to assign WIP, check DB first to see if WIP assigned already. If there is WIP, remove from tag and send relevant info </li>
<li> Small batch 2: implement front-end view for supervisor. New component to display all of WIPs that were overwritten </li>
<li> Small batch 3: new end times entered by supervisor must be updates to database </li>

</ul>

<em>Rabbit Holes</em>
<ul>
<li> Do not get caught up in the front-end </li>
<li> Prioritize back-end functionality of t-end </li>
</ul>

<strong>Sonya’s Pitch </strong>
<em>Problem</em>
<ul>
<li> Tags are displayed in lists </li>
<li> Difficult to gather information quickly </li>
</ul>

<em>Appetite</em>
<ul>
<li> To create a more streamlined way to get tag information </li>
</ul>

<em>Solution</em>
<ul>
<li> Create a scaled map that shows location of tags </li>
<li> Users are use to navigating a map </li>
<li> Tags will be placed in different zones </li>
</ul>

<em>Rabbit Holes</em>
<ul>
<li> Too much time spent on putting all tag information on quick view of map </li>
<li> This can make scaled map look too cluttered </li>
<li> Organization is key and clarity is not lost </li>
</ul>

<em>No Gos</em>
<ul>
<li> Do not include editable fields do tag information </li>
<li> Purpose of this </li>
</ul>

<strong>Gabriel’s Pitch </strong>
<em>Problem</em>
<ul>
<li> How to quantify subjective measures like performance and durability </li>
</ul>

<em>Appetite</em>
<ul>
<li> Tweak front-end and back-end to fit requirements of hockey rink </li>
</ul>

<em>Solution</em>
<ul>
<li> Create new front-end view of hockey rink with analytics </li>
</ul>

<em>Rabbit Holes</em>
<ul>
<li> Begin developing new code instead of reusing already implemented code </li>
</ul>



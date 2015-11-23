<h3>Flash Vars:</h3>
<table width='100%' border='1'>
<blockquote><tr>
<blockquote><td width='50'><strong>Variable </strong></td>
<td width='50'><strong>Type</strong></td>
<td width='300'><strong>Description</strong></td>
</blockquote></tr>
<tr>
<blockquote><td width='50'>channel</td>
<td width='50'>String</td>
<td width='300'><p>Multicast Group Name: This is used in making netstream connections or creating private groups using NetGroups</p>    </td>
</blockquote></tr>
<tr>
<blockquote><td width='50'>rtmfp</td>
<td width='50'>String</td>
<td width='300'>Your RTMFP url: This can be your cirrus or FMS based rtmfp url</td>
</blockquote></tr>
<tr>
<blockquote><td width='50'>stream</td>
<td width='50'>String</td>
<td width='300'>Multicast stream name:</td>
</blockquote></tr>
<tr>
<blockquote><td width='50'>isPrivate</td>
<td width='50'>Boolean</td>
<td width='300'>Use private group : Specifies whether to create a NetGroup or not.</td>
</blockquote></tr>
</table></blockquote>


<h3><strong>SWFObject Example:</strong></h3>
<p>
<pre>
<script type="text/javascript" src="js/swfobject.js"><br>
<br>
Unknown end tag for </script><br>
<br>
<br>
<script type="text/javascript"><br>
var flashvars = {};<br>
flashvars.channel = "somechannelname";<br>
flashvars.rtmfp = "rtmfp://p2p.rtmfp.net/xxxxxxxxxxxxxxxxxxxxxxxxx";<br>
flashvars.stream = "livestream";<br>
var params = {};<br>
params.quality = "autohigh";<br>
params.scale = "noscale";<br>
params.salign = "tl";<br>
params.allowfullscreen = "true";<br>
params.allowscriptaccess = "sameDomain";<br>
var attributes = {};<br>
attributes.id = "peerviewer";<br>
attributes.name = "peerviewer";<br>
swfobject.embedSWF("viewer.swf", "myAlternativeContent", "320", "240", "10.1.0", "swf/playerProductInstall.swf", flashvars, params, attributes);<br>
<br>
function Alert(params)<br>
{<br>
alert(params);<br>
}<br>
<br>
<br>
Unknown end tag for </script><br>
<br>
<br>
</pre>
</p>

<h3><strong>Special Notes:</strong></h3>
<p>The player resolves any group name specified to <span>swfdomain/channel</span> to keep the group unique as far as possible. Hence your broadcasting application must broadcast in the same manner to be able to reach viewer.</p>
<p>Eg: mychannel resolves to localhost/mychannel.</p>
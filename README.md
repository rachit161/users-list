# users-list
<html>
<style type="text/css">
body  {
  background-image: url("https://previews.123rf.com/images/nicoelnino/nicoelnino1701/nicoelnino170100597/70853397-smart-home-automation-interface-with-user-in-background-touching-button-to-control-house-equipments.jpg");
  background-color: #cccccc;
}
#navlist { 
            background-color: #0074D9; 
            position: absolute; 
            width: 100%; 
        } 
          
        #navlist a { 
            float:left; 
            display: block; 
            color: #f2f2f2; 
            text-align: center; 
            padding: 12px; 
            text-decoration: none; 
            font-size: 15px; 
        } 
        .navlist-right{ 
            float:right; 
        } 
  
 
        #navlist a:hover { 
            background-color: #ddd; 
            color: black; 
        } 
          
        .search input[type=text]{ 
            width:300px; 
            height:25px; 
            border-radius:25px; 
            border: none; 
  
        } 
          
        .search{ 
            float:right; 
            margin:7px; 
  
        } 
          
        .search button{ 
            background-color: #0074D9; 
            color: #f2f2f2; 
            float: right; 
            padding: 5px 10px; 
            margin-right: 16px; 
            font-size: 12px; 
            border: none; 
            cursor: pointer; 
        }  

.pg-normal {
color: #000000;
font-size: 15px;
cursor: pointer;
background: #D0B389;
padding: 2px 4px 2px 4px;
}

.pg-selected {
color: #fff;
font-size: 15px;
background: #000000;
padding: 2px 4px 2px 4px;
}

table.yui {
font-family:arial;
border-collapse:collapse;
border: solid 3px #7f7f7f;
font-size:small;
width: 100%;
height: 50%;
}

table.yui td {
padding: 5px;
border-right: solid 1px #7f7f7f;
}

table.yui .even {
background-color: #F0FFFF;
}

table.yui .odd {
background-color: #A9A9A9;
}

table.yui th {
border: 1px solid #7f7f7f;
padding: 5px;
height: auto;
background: #4CAF50;
}

table.yui th a {
text-decoration: none;
text-align: center;
padding-right: 20px;
font-weight:bold;
white-space:nowrap;
}

table.yui tfoot td {
border-top: 1px solid #7f7f7f;
background-color:#E1ECF9;
}

table.yui thead td {
vertical-align:middle;
background-color:#E1ECF9;
border:none;
}

table.yui thead .tableHeader {
font-size:larger;
font-weight:bold;
}

table.yui thead .filter {
text-align:right;
}

table.yui tfoot {
background-color:#E1ECF9;
text-align:center;
}

table.yui .tablesorterPager {
padding: 10px 0 10px 0;
}

table.yui .tablesorterPager span {
padding: 0 5px 0 5px;
}

table.yui .tablesorterPager input.prev {
width: auto;
margin-right: 10px;
}

table.yui .tablesorterPager input.next {
width: auto;
margin-left: 10px;
}

table.yui .pagedisplay {
font-size:10pt; 
width: 30px;
border: 0px;
background-color:#E1ECF9 ;
text-align:center;
vertical-align:top;
}
</style>
<script type="text/javascript">

function Pager(tableName, itemsPerPage) {

this.tableName = tableName;

this.itemsPerPage = itemsPerPage;

this.currentPage = 1;

this.pages = 0;

this.inited = false;

this.showRecords = function(from, to) {

var rows = document.getElementById(tableName).rows;


for (var i = 1; i < rows.length; i++) {

if (i < from || i > to)

rows[i].style.display = 'none';

else

rows[i].style.display = '';

}

}

this.showPage = function(pageNumber) {

if (! this.inited) {

alert("not inited");

return;

}

var oldPageAnchor = document.getElementById('pg'+this.currentPage);

oldPageAnchor.className = 'pg-normal';

this.currentPage = pageNumber;

var newPageAnchor = document.getElementById('pg'+this.currentPage);

newPageAnchor.className = 'pg-selected';

var from = (pageNumber - 1) * itemsPerPage + 1;

var to = from + itemsPerPage - 1;

this.showRecords(from, to);

}

this.prev = function() {

if (this.currentPage > 1)

this.showPage(this.currentPage - 1);

}

this.next = function() {

if (this.currentPage < this.pages) {

this.showPage(this.currentPage + 1);

}

}

this.init = function() {

var rows = document.getElementById(tableName).rows;

var records = (rows.length - 1);

this.pages = Math.ceil(records / itemsPerPage);

this.inited = true;

}

this.showPageNav = function(pagerName, positionId) {

if (! this.inited) {

alert("not inited");

return;

}

var element = document.getElementById(positionId);

var pagerHtml = '<span onclick="' + pagerName + '.prev();" class="pg-normal"> « Prev </span> ';

for (var page = 1; page <= this.pages; page++)

pagerHtml += '<span id="pg' + page + '" class="pg-normal" onclick="' + pagerName + '.showPage(' + page + ');">' + page + '</span> ';

pagerHtml += '<span onclick="'+pagerName+'.next();" class="pg-normal"> Next »</span>';

element.innerHTML = pagerHtml;

}

}

</script>
<table id="tablepaging" class="yui" align="center">
<thead>

<tr> 
<th>id</th>
<th>First_name </th>
<th>Last_name</th>
<th>email </th>
</tr>
</thead>
<tbody>
<div class="search"> 
              
            <form action="#"> 
                <input type="text"
                    placeholder=" Search "
                    name="search"> 
                <button> 
                    <i class="fa fa-search"
                        style="font-size: 18px;"> 
                    </i> 
                </button> 
            </form> 
        </div> 
    </div> 

<tr class="even">
<td>1 </td>
<td> Michael</td>
<td>Lawson </td>
<td>michael.lawson@reqres.in </td>
</tr>
<tr class="odd">

<td>2 </td>
<td>Lindsay </td>
<td>Ferguson </td>
<td>lindsay.ferguson@reqres.in </td>
</tr>

<tr class="even">
<td>3 </td>
<td> Tobias</td>
<td>Funke</td>
<td>tobias.funke@reqres.in </td>
</tr>

<tr class="odd">

<td>4 </td>
<td>Byron</td>
<td>Fields </td>
<td>byron.fields@reqres.in </td>
</tr>

<tr class="even">
<td>5 </td>
<td> George</td>
<td>Edwards</td>
<td>george.edwards@reqres.in </td>
</tr>

<tr class="odd">

<td>6 </td>
<td>Rachel</td>
<td>Howell</td>
<td>rachel.howell@reqres.in </td>
</tr>

<tr class="even">
<td>7 </td>
<td> Herrod</td>
<td>Chandler</td>
<td>herrod.chandler@erer.in </td>
</tr>

<tr class="odd">
<td>8</td>
<td>Rhona</td>
<td>Davidson</td>
<td>rhona.davidson@jsf.in</td>
     
</tr>
<tr class="even">
<td>9</td>
<td>Colleen</td>
<td>Hurst</td>
<td>collen.hurst@efe.in</td>

</tr>
<tr class="odd">
<td>10</td>
<td>Sonya</td>
<td> Frost</td>
<td>sonya.frost@sdsf.in/td>
     
</tr>
<tr class="even">
<td>11</td>
<td>Jena </td>
<td>Gaines</td>
<td>jena.gaines@fdgsd.in</td>
      
</tr>
<tr class="odd">
<td>12</td>
<td>Quinn</td>
<td>Flynn</td>
<td>quinn.flynn@sbhfs.in</td>
     
 </tr>

</tbody>
</table>

<div id="pageNavPosition" style="padding-top: 20px" align="center">
</div>
<script type="text/javascript"><!--
var pager = new Pager('tablepaging', 4);
pager.init();
pager.showPageNav('pager', 'pageNavPosition');
pager.showPage(1);
</script>
</html>

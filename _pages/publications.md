---
title: "The Group - Publications"
layout: gridlay
excerpt: "The Group -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Highlights

(For a full list see [below](#full-list) or go to [Google Scholar](https://scholar.google.com/citations?user=QnYCqUsAAAAJ&hl=en))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Full List
<!--
{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
-->

Conference papers are after journal articles.

<style>
div#yearTitle{
	padding-bottom:1em;
}
td.year  {
	font-size : 9pt;
	font-weight : bold;
	padding-top : 2px;
	padding-right : 9px;
	z-index : 10;
}
.maintext {
  background-color: white;
  padding: 2em;
  margin-top: 0em;
  margin-left: 2px;
  margin-right: 2px;
 }
.pubtext {
  clear: right;
  margin-top: 3em;
  /*border-top: 1px  #c0c0e0; */
  padding-top: 2em;
  height: 99%;
  min-height: 200px;
 }
.expbutton {
  font-size: 7pt;
  float:left; margin-right: 7px;
  width: 0.7em;
  height: 1em;
  /*background-color: #f0fff8;*/
  padding-left:2px; padding-right:2px;
  padding-bottom:2px;
  border:1px solid #e0e0e0;
  color: #333399;
}
.publication {
  /*margin-top: 0.1em*/;
  padding: 0.1em;
  z-index: 10;
/* margin-bottom:2em;
  margin-top: 0.5em;
  padding: 0.5em;
*/
  margin-left: 2em;
/*
  border-top: 1px solid #e0e0e0;
  border-right: 1px solid #e0e0e0;
  border-left: 1px solid #e0e0e0;
*/
  font-size: 12pt;
  /* trigger IE layout mode */
  min-width:0px;
/*  overflow: auto; */
/*  background-color: #f8faf8; */
 }
.noyeartitle {
  color: #333399;
  border-bottom: 2px solid #333399;
  margin-top: 2em;
  padding-bottom: 4px;
/*  font-family: sans-serif; */
  font-size: 14pt;
 }
.yearindent {
/*  margin-left: 2em; */
 }
 .yeartitle, .yearsep{
 clear: both;
 }
.dup {
  color: #a0a0b0;
 }
.refdiv {
  border-left: 2px solid transparent;
  /*background-color: white; */
  color : #303030;
  padding-top : 2px;
  padding-bottom : 2px;
  margin : 0px;
  font-size : 11pt;
  border-bottom : 1px dotted #f0f0f0;
 }
.control {
  text-decoration: none;
 }
.contact {
  float: right;
  border : 1px solid #dcdcdc;
  padding: 1em;
  margin-left: 1em;
  background-color: #ffffe8;
 }
.controls {
  float: right;
}
.controls a {
  color: #333399;
 }
.publistlink {
  text-decoration: none;
  color: black;
 }
.formhelp {
  font-style: italic;
  color: #a0a0a0;
 }
.formfield {
/*  font-weight: bold; */
  font-size: 8pt;
 }
.formoptfield {
  font-size: 8pt;
  color: #606060;
 }
.flright {
  float: right;
 }
/* Styles for the reference items */
.abstract {
  margin: 1em;
  margin-left: 3em;
  font-style: italic;
  color: #404080;
  min-width: 0px;
 }
span {
  min-width: 0px;
  _zoom: 1; /* trigger hasLayout in IE6 to work around IE bugs */
 }
/* Add a layout class to an a to get it to display in IE6 */
a.layout, div.layout {
  _zoom: 1;
 }
div {
  min-width: 0px;
 }
.note {
  margin: 1em;
  margin-left: 3em;
  color: #222222;
/*  font-family: verdana, arial, sans; */
  min-width: 0px;
}
.notags {
  display: inline;
  margin: 1em;
  margin-left: 3em;
  color: #333399;
  font-weight: bold;
  font-style: italic;
 }
.journal, .booktitle {
  font-style: italic;
 }
.title {
  color : #404040;
  font-weight: bold;
  text-decoration: none;
}
.editor {
  color: #999999;
 }
 .amaProceedings{
 color:#303030;
 }
.fulltextlinks {
  float: right;
  padding-left: 12px;
  padding-bottom: 4px;
  width: auto;
  display:inline;
}
.doilink, .doilink:hover, .repolink, .repolink:hover, .pubmedlink, .pubmedlink:hover {
  font-size:7pt;
 }
 .doilink,.htmllink,.pdflink,.pubmedlink,.repolink{
 margin-right: 4px;
 }
.indexpad {
  margin-left: 2em;
  /*padding-top: 2em;*/
 }
.indexsub {
  margin-left: 2em;
  padding-top: 2em;
 }
.indexref {
  clear:both;
  padding: 4px;
 }
/* For pubmed entries present in list */
.present {
  filter: alpha(opacity=70);
  filter: progid:DXImageTransform.Microsoft.Alpha(opacity=70);
  _zoom:1;
  opacity: 0.7;
  border-left: 1px solid orange;
  border-right: 1px solid orange;
  margin-bottom: 8px;
 }
/* For updated pubmed entries */
.medline {
  _zoom:1;
  border: 1px solid blue;
  margin-bottom: 8px;
 }
.yearsub {
  float: right;
  font-style : italic;
  font-weight: normal;
/*  color: #339933; */
 }
.yearsep {
  font-size: 12pt;
  font-weight: bold;
  color:#666666;
  padding-top : 2px;
  width:80px;
  word-wrap:break-word;
/*  padding-right: 1em; */
}
.noyearsep {
  font-weight: bold;
  color: #666699;
  margin-top: 2em;
  margin-bottom: 1em;
  margin-left: 0em;
  font-size: 120%;
  border-bottom: 1px dotted #cccccc;
}
.publist {
/*  font-family: sans-serif, bookman, serif; */
 }
a.pdflink, a.htmllink {
  color: green;
  text-decoration: none;
 }
div.thumbdiv {
  float:right;
/*   margin-right:1em; */
  margin-left:1em;
  margin-bottom:1em;
  border-right:1px dotted #ddd;
  border-bottom:1px dotted #ddd;
}
img.thumbimg {
  width:80px;
}
a.authorlink {
  font-size:11pt;
  cursor:pointer;
  color: #303030;
}
a.authorlink:hover {
  color: #303030;
  font-size:11pt;
  text-decoration:underline;
}
.editcontrols {
  color:white;
  font-size: 10pt;
  background-color:#808080;
  margin:0px;
  padding:4px;
 }
.atag {
  text-decoration:none;
  color:green;
 }
.aauthor {
  text-decoration:none;
  color:blue;
 }
.selbutton {
  border: 1px inset green;
  background-color: #e8e8e8;
  padding: 0.3em;
  display: inline;
  color: green;
  font-weight: bold;
 }
.unselbutton {
  font-weight: bold;
  color: #909090;
  border: 1px outset #c0c0c0;
  padding: 0.3em;
  text-decoration: none;
 }
.selref {
  /* border : 1px dashed #808080; */
}
.selref span.refbody {
	background-color : #f6c384;
	 border : 1px dotted #b0b0b0;
}
.hideit {
  display: none;
 }
.refdiv {
  margin-left: 1em;
  margin-right: 1em;
  padding: 0.1em;
 }
.title {
  cursor: pointer;
 }
.notitle:hover {
  background-color: #e0fcf0;
 }
.shelp{
  font-style : italic;
  color: #a0a0a0;
}
span.selcoll {
  background-color: #66ff66;
  cursor: pointer;
}
span.unselcoll {
  cursor: pointer;
}
a.amatitle {
  font-weight: normal;
}
a.expand{
	float:left;
}
a.harvardtitle{
	font-weight:normal;
}
a.tagText{
	font-style:italic;
}
.sats{
	display:none;
}
a.arrowDown{
	float:left;
	visibility:inherit;
	cursor :pointer;
}
a.arrowUp{
	float:left;
	visibility:inherit;
	cursor :pointer;
	margin-left:0.5em;
}
a.whiteBorder{
	position:relative;
	top:-80px;
}
div.refCommonProperties{
	border:1px solid white;
	margin-left:2em;
}
div.tool{
	float:right;
	padding-left:3em;
}
div.publishDetail{
	padding-left:12px;
	float:right;
}
a.fullText{
	color:red;
	text-decoration:none;
}
a.icons{
	float:right;
}
div.aPublication{
	margin-botton:3em;
	text-align:right;
	margin-right:4em;
	font-style:italic;
	color:#a0a0a0;
}
table.sameYearTable{
	width:95%;
	table-layout:fixed;
	border-collapse:separate;
	border-spacing:0px;
	padding:0px;
}
.findhighlight{
 	background-color : #FFFACD;
/* 	border:1px solid; */
/*     border-color:#FF69B4; */
}
</style>

<div class="row well" style='padding: 20px'>
<div id='publistdiv'>Loading publications...</div>
</div>

<div class="row well" style='padding: 20px'>
<div id='tagslist' style='display:none;'></div>
<div id='authorslist' style='display:none;'></div>
</div>

<script src='//publicationslist.org/data/satra/publist.js'></script>

<script>
var details = {"firstname":"Satrajit","middlename":"S","lastname":"Ghosh",
"email":"satra@mit.edu","website":"\/\/www.mit.edu\/~satra","address":"","biosketch":""}
;
var readonly = '1';
var rootpath = '//publicationslist.org/';
var ownpage = '1';
var userid = 'satra';
var mode = 'publish';
var nothumbs = 0;
var publistBrand = "PublicationsList.org";
var localInstall = 0;
var citationFormat = "default";
var previewMode = '';
var uptodate = '1';
var recent = false;
</script>


<script src='//publicationslist.org/schema.js?'></script>
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
<script src='//publicationslist.org/data/satra/BROWSER.js?1384435485'></script>
<script src='//publicationslist.org/data/satra/DOM.js?1384435485'></script>
<script src='//publicationslist.org/data/satra/pubutil.js?1434354606'></script>
<script src='//publicationslist.org/data/satra/pubinit.js?1384435485'></script>

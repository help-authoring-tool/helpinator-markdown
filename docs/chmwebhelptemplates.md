## HTML-based Templates

Each CHM/WebHelp template consists of two file groups:


1. Required files. Usually templates' main HTML page template and corresponding CSS file.
2. Additional files. Images used by template, scripts and etc.


In predefined templates there's jqueryui.zip file that contains JQuery UI theme for WebHelp (left pane with TOC, Index and Search). Inside it there's jqueryui.css and jqueryui.js files and "images" folder with images used by this theme.


HTML templates use several tags, enclosed in &#123;&#37;&#37;&#125;:


<table>
<tr><th>TRVTableCellData</th><th>TRVTableCellData</th></tr><tr><td><p>
<b>Tag</b>
</p></td><td><p>
<b>Meaning</b>
</p></td></tr><tr><td><p>
TITLE
</p></td><td><p>
Title of the current topic
</p></td></tr><tr><td><p>
BREADCRUMBS
</p></td><td><p>
Place for breadcrumbs links
</p></td></tr><tr><td><p>
PREVNEXTTOPIC
</p></td><td><p>
Links to previous and next topics, combined
</p></td></tr><tr><td><p>
PREVTOPIC
</p></td><td><p>
Link to previous topic
</p></td></tr><tr><td><p>
NEXTTOPIC
</p></td><td><p>
Link to next topic
</p></td></tr><tr><td><p>
PREVTOPIC_INCL
</p></td><td><p>
Link to previous topic, but instead of "Previous" text it uses HTML between this tag and END_PREVTOPIC_INCL tag.
</p></td></tr><tr><td><p>
NEXTTOPIC_INCL
</p></td><td><p>
Same as above but for next topic
</p></td></tr><tr><td><p>
SEEALSO
</p></td><td><p>
Lists related topics based on keywords match.
</p></td></tr></table>


You can also use project variables inside templates.


![htmltemplates.png](images/htmltemplates.png "htmltemplates.png")


![htmltemplates1.png](images/htmltemplates1.png "htmltemplates1.png")


**Adapting WebHelp to your website**


You can also adapt WebHelp appearance to the style of your website using WebHelp header and footer. This fields are not required, if empty WebHelp will fill entire browser page. When filled, header and footer will appear in separate frames.


![htmltemplates2.png](images/htmltemplates2.png "htmltemplates2.png")

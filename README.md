squarespace-js-snippets
=======================

### edit the date format of a blog post to mm/dd/yyyy

<script> /* ::::::::::::::::::::::::::::::::::::::::::::: */ var month=new Array(12); month[0]="01"; month[1]="02"; month[2]="03"; month[3]="04"; month[4]="05"; month[5]="06"; month[6]="07"; month[7]="08"; month[8]="09"; month[9]="10"; month[10]="11"; month[11]="12"; Y.use('node', 'node-load', function(Y) { Y.on('domready', function() { /* ::::::::::::::::::::::::::::::::::::::::::::: ::: Reformat published date (Blog) */ Y.all('time.published').each( function() { var pdate = new Date(this.getAttribute('datetime')); this.setHTML(month[pdate.getMonth()] + " " + pdate.getDate() + " " + pdate.getFullYear()); } ); // .published /* ::::::::::::::::::::::::::::::::::::::::::::: ::: Reformat time since string */ Y.all('time.timestamp').each( function() { var tdate = new Date(this.getAttribute('datetime')); this.setHTML(tdate.getDate() + " " + month[tdate.getMonth()] + " " + tdate.getFullYear()); } ); // .timestamp (.timesince) }); // Y.on }); </script>

http://answers.squarespace.com/questions/40751/how-to-edit-the-date-format-of-a-blog-post-to-mmddyyyy

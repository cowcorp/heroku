# heroku
Source for cowcorp.herokuapp.com<br>
<br>
To do development in github.com:<br><ul>
<li>Select the cowcorp/heroku repository.</li>
<li>Select the branch dropdown, and change from "master" by typing "Development".</li>
<li>Edit multiple files as needed.</li>
<li>Test these edits by going to Heroku's pipeline page, dropdown the cowcorp-development menu, and selecting to (manually) deploy that branch.</li></ul>
<br>
When the development is ready for production:<br><ul>
<li>In github.com: go to the top level of cowcorp/heroku repository, create a new PullRequest, select SquashAndMerge (and confirm that), and then delete "Development" branch when suggested.</li>
<li>Heroku's production pipeline stage is set to automatically build when it detects this change to github's "master" branch.</li></ul>
<br>
A Heroku application is:<br><ul>
<li>Written in Ruby, Node.js, Java, Python, Clojure, Scala, Go or PHP.</li>
<li>Consists of source, makefile-equivalent, and a "procfile" that describe what to execute.</li></ul> 

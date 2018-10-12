# heroku
Source for cowcorp.herokuapp.com<br>
<br>
To do development in github.com:<br>
Select the cowcorp/heroku repository.<br>
Select the branch dropdown, and change from "master" by typing "Development".<br>
Edit multiple files as needed.<br>
Test these edits by going to Heroku's pipeline page, dropdown the cowcorp-development menu, and selecting to (manually) deploy that branch.<br>
<br>
When the development is ready for production:<br>
In github.com: go to the top level of cowcorp/heroku repository, create a new PullRequest, select SquashAndMerge (and confirm that), and then delete "Development" branch when suggested.<br>
Heroku's production pipeline stage is set to automatically build when it detects this change to github's "master" branch.

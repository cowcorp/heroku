# heroku
<p>Source for cowcorp.herokuapp.com</p>
<p>
My (cowcorpSalesforce@gmail.com account's) Heroku tool already contains a "cowcorp" project for building cowcorp.herokuapp.com (things like knowing which external add-ons are needed).
If that were somehow to ever get destroyed, it could be re-generated from a template.
That re-generation is possible because this source code is hosted in github, and app.json specifies the template.
Clicking here <a href="https://heroku.com/deploy?template=https://github.com/cowcorp/heroku"><img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy"></a> causes the re-generation (this button's URL could have skipped its template setting, because the URL refers to itself).
</p>
<p>To do development in github.com:</p><ul>
<li>Select the cowcorp/heroku repository.</li>
<li>Select the branch dropdown, and change from "master" by typing "Development".</li>
<li>Edit multiple files as needed.</li>
<li>Test these edits by going to Heroku's pipeline page, dropdown the cowcorp-development menu, and selecting to (manually) deploy that branch.</li></ul>
<p>When the development is ready for production:</p><ul>
<li>Edit configuration variables. Source code condition statements can use those settings, by reading those settings via environment variables.</li>
<li>In github.com: go to the top level of cowcorp/heroku repository, create a new PullRequest, select SquashAndMerge (and confirm that), and then delete "Development" branch when suggested.</li>
<li>Heroku's production pipeline stage is set to automatically build when it detects this change to github's "master" branch.</li></ul>
<br>
A Heroku application:<br><ul>
<li>An application is written in Ruby, Node.js, Java, Python, Clojure, Scala, Go or PHP.</li>
<li>The application consists of source, makefile-equivalent, and a "procfile" that describes a "dyno formation" (which resultant process(es) to run on how many "dyno" execution Unix sandboxes). If the process is named "web", then it can receive HTTP traffic.</li>
<li>When that information is deployed to Heroku, Heroku builds a "slug" (adding object files) by using that language's "buildpack". For new languages, custom buildpacks can be created.</li>
<li>If you want persistence between dyno sandboxes, you need to use an external add-on such as a database. Even file modifications in one sandbox are not seen in other sandboxes.</li>
<li>A dyno runs a "execution-release" (development or production): a slug; plus configuration variable settings; plus add-ons. A new build is triggered by a change to any of these three things.</li>
<li>Logplex is a running buffer of log messages from both application and system processes.</li></ul>

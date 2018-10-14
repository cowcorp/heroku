# cowcorp/cowcorp-opensource.herokuapp.com
<p>Source for <nobr><code>cowcorp-opensource.herokuapp.com</code></nobr></p> 
<p>
My <nobr>(<code>cowcorpSalesforce@gmail.com</code> account's) Heroku</nobr> tool already contains a "cowcorp-opensource" project for building <nobr><code>cowcorp-opensource.herokuapp.com</code></nobr> (things like knowing which external add-ons are needed).
If that were somehow to ever get destroyed, it could be re-generated from a template.
That re-generation is possible because this opensource source code is hosted in github, and app.json specifies the template.
Clicking here <a href="https://heroku.com/deploy?template=https://github.com/cowcorp/cowcorp-opensource.herokuapp.com"><img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy"></a> causes the re-generation (this button's URL could have skipped its <nobr><code>template</code></nobr> setting, because the URL refers to itself).
</p>
<p>To do development in github.com:</p>
<ul><li>Select the <nobr><code>cowcorp/cowcorp-opensource.herokuapp.com</code></nobr> repository.</li>
<li>Select the branch dropdown, and change from "master" by typing "development".</li>
<li>Edit multiple files as needed.</li>
<li>Test these edits by going to Heroku's pipeline page, dropdown the cowcorp-opensource-development menu, and selecting to (manually) deploy that branch.</li></ul>
<p>When the development is ready for production:</p>
<ul><li>Edit configuration variables. Source code condition statements can use those settings, by reading those settings via environment variables.</li>
<li>In <nobr><code>github.com</code>:</nobr> go to the top level of <nobr><code>cowcorp/cowcorp-opensource.herokuapp.com</code></nobr> repository, create a new PullRequest, select SquashAndMerge (and confirm that), and then delete "development" branch when suggested.</li>
<li>Heroku's production pipeline stage is set to automatically build when it detects this change to github's "master" branch.</li></ul>

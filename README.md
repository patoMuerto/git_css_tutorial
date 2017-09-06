
OK, here is a workflow with examples.  I set up a repository on Github that you can practice with.  You can find it at,

   https://github.com/patoMuerto/git_css_tutorial.git

There are a couple of principles that we try to follow with a Configuration Management (CM) system.  

   a) You should always have a branch that is working.  To keep the branch working you only merge working code into that branch.  It is most often called 'master' but sometimes you will have 2 or 3 branches where things must always work.  They are usually for new component or experimental code.

   b) When ever you make a significant change you create a new branch.  A significant change would be considered a new feature, or even when you add a file.  This is for several reasons, mostly for how coding groups organize and execute a project.  But, it is also for your benefit because it organizes it so you can quickly try new things out and it will be isolated until you get it to a decent working state.

   c) Commit often.  As soon as you have something working, or just want to mark your progress, do a commit.  Be verbose with the comments.  It helps if you develop a format and try to follow it.  More on that later.


The process in a nutshell:


   Pre-step:  Obviously you need to clone the repository from github

      git clone https://github.com/patoMuerto/git_css_tutorial.git

   Steps:
   1) checkout master,  it has the latest working version

      git checkout master

   2) get any updates from github

      git fetch

         or

      git pull

   3) create new branch that will include your new feature or change.

      git checkout -b <new_feat>

         NOTE: <xxxxxxx> is a standard that represents that you are
              to supply the name inside the <>.  You dont include the <>.

   4) add file w/ some new features.  You can check what files you 
   edited and added by checking status,

      git status

   5) Add file to be tracked

      git add <new_file_name>

   6) Commit with message

      git commit -m "NEW_FEAT_1: This commit includes a new README.md"

         NOTE: The -m stands for add message.  Sometimes if you don't include
               it an editor might pop up.  Sometimes it uses an obscure editor.

   7) Keep editing, adding and commiting until you have the new feature working
      or it is at the end of the day and you need to back it up.  Then push it.

      git push origin <new_feat>

         NOTE: origin is the default name of the repository you cloned from.
               In this case it is github.  You can see it using the command

                  git remote -v

   At this point you have the new feature working.  Since it is based on master
   it should have all the previous features as well.  So now you need to merge
   it with master to "share" it with other people.  Or, just collect all the
   new features into one location.  So now merge w/ master

   8) checkout master

      git checkout master

   9) get any changes from github

      git fetch

   10) merge with new feature branch

      git merge <new_feat>

   11) test to make sure things work

   12) push master to github

      git push origin master

   13) repeat with the next feature.


This should be enough to get you started.  

      


Users-Mac:dev User$ git clone my-website.ca/ my-website_heroku
Cloning into 'my-website_heroku'...
done.
Checking out files: 100% (2267/2267), done.
Users-Mac:dev User$ cd my-website_heroku/
Users-Mac:my-website_heroku User$ heroku create -s cedar
Creating my-heroku-app-1234... done, stack is cedar-10
https://my-heroku-app-1234.herokuapp.com/ | https://git.heroku.com/my-heroku-app-1234.git
Git remote heroku added
Users-Mac:my-website_heroku User$ heroku config:add BUILDPACK_URL=https://github.com/mchung/heroku-buildpack-wordpress.git
Setting config vars and restarting my-heroku-app-1234... done, v3
BUILDPACK_URL: https://github.com/mchung/heroku-buildpack-wordpress.git
Users-Mac:my-website_heroku User$ git push heroku master
Counting objects: 2196, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2094/2094), done.
Writing objects: 100% (2196/2196), 10.00 MiB | 301.00 KiB/s, done.
Total 2196 (delta 233), reused 0 (delta 0)
remote: Compressing source files... done.
remote: Building source:
remote:
remote: -----> Fetching custom git buildpack... done
remote:
remote:  !     Push rejected, no Cedar-supported app detected
remote: HINT: This occurs when Heroku cannot detect the buildpack
remote:       to use for this application automatically.
remote: See https://devcenter.heroku.com/articles/buildpacks
remote:
remote: Verifying deploy...
remote:
remote: !   Push rejected to my-heroku-app-1234.
remote:
To https://git.heroku.com/my-heroku-app-1234.git
 ! [remote rejected] master -> master (pre-receive hook declined)
error: failed to push some refs to 'https://git.heroku.com/my-heroku-app-1234.git'
Users-Mac:my-website_heroku User$ git add -A
Users-Mac:my-website_heroku User$ git commit -a -m "heroku"
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean
Users-Mac:my-website_heroku User$

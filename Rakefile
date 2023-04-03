require 'rubygems'
require 'optparse'
require 'yaml'

task :build do
   desc "runs jekyll to generate _site/"
   system "bundle exec jekyll build"
end

task :setupdeploy do
   desc "adds the remote that autodeploys on lly.fr"
   system "git remote add deploy nileane@lly.fr:~/1pct-deploy"
end

task :deploy do
   desc "deploys @ nileane@lly.fr:~/1pct-deploy"
   system "git push origin master && git push deploy master"
end

task :commit do
   desc "commits changes"
   system "git add -A && git commit -m 'Updated'"
end

task :serve do
   desc "runs jekyll server with autoregen enabled"
   system "bundle exec jekyll serve --watch"
end

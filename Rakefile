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
   desc "runs git to pull new code & jekyll to generate _site/"
   system "git push origin master && git push deploy master"
end

task :serve do
   desc "runs jekyll server with autoregen enabled"
   system "bundle exec jekyll serve --watch"
end

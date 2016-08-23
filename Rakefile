require 'html-proofer'

task :default => [:test]

task :build do
  sh 'bundle exec jekyll build'
end

task :test => [:build] do
  HTMLProofer.check_directory('./_site', {:disable_external => true, :url_ignore => ['#']}).run
end

task :deploy => [:test] do
  cp_r Dir.glob('_site/*'), 'dist/'
end

require 'html-proofer'

task :default => [:proof_html]

task :proof_html do
  sh "bundle exec jekyll build"
  HTMLProofer.check_directory("./_site", {:disable_external => true, :url_ignore => ["#"]}).run
end

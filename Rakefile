task :default => [:proof_html]

task :proof_html do
  require 'html-proofer'
  HTMLProofer.check_directory("./_site").run
end

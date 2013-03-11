desc "Compile _less/blog.less to stylesheets/blog.css (requires the less gem)"
task :css do
  sh "lessc _less/blog.less > stylesheets/blog.css"
end

desc "Deploy site to GH-PAGES"
task :deploy do
  puts "Please EDIT the :deploy task."
end

desc "publish BRANCH to REPO"
task :publish do
  puts "git push ??? REPO:gh-pages"
  # system("git push dinky-theme DESTINATION:gh-pages")
end

# desc "setup all repos"
# git remote add github git@github.com:wbzyl/wbzyl.github.com.git

desc "deploy branch dinky-theme to wbzyl.github.com master branch"
task :deploy do
  #     git push remote_name source_ref:destination_ref
  puts "git push github      dinky-theme:master"
  # system("git push dinky-theme DESTINATION:gh-pages")
end

# desc "publish to all branches"
# task :publish do
#   LANGS.each do |lang|
#     system("git push #{lang} #{lang}:gh-pages")
#   end
# end

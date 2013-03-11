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

desc "deploy branch dinky-theme to wbzyl.github.com master branch"
task :deploy do
  puts "??? git push origin dinky-theme:master"
  # system("git push dinky-theme DESTINATION:gh-pages")
end

# LANGS = %w[de en es fr he it ja ko nl pt-br ru sv]

# desc "setup all branches"
# task :setup do
#   LANGS.each do |lang|
#     system("git checkout -t -b #{lang} origin/#{lang}")
#     system("git remote add #{lang} git@github.com:gitready/#{lang}.git")
#   end
#   system("git checkout en")
# end

# desc "publish to all branches"
# task :publish do
#   LANGS.each do |lang|
#     system("git push #{lang} #{lang}:gh-pages")
#   end
# end

desc "Compile _less/blog.less to stylesheets/blog.css (requires the less gem)"
task :css do
  sh "lessc _less/blog.less > stylesheets/blog.css"
end

# ----

desc "Setup: add wbzyl/wbzyl.github.com.git as remote"
task :setup do
  sh "git remote add github git@github.com:wbzyl/wbzyl.github.com.git"
end

desc "Deploy dinky-theme branch to wbzyl.github.com master branch"
task :deploy do
  #     git push remote_name source_ref:destination_ref
  puts "git push github +dinky-theme:master"
end

desc "Deploy dinky-theme branch to gh-pages wbzyl/test repo"
task :deploy_to_repo do
    sh "git push origin dinky-theme:gh-pages"
end

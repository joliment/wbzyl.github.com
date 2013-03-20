# ----
#
# User Pages

desc "Add wbzyl/wbzyl.github.com.git as remote"
task :setup_user_pages do
  sh "git remote add user_pages git@github.com:wbzyl/wbzyl.github.com.git"
end

desc "Deploy DINKY THEME to wbzyl.github.com User Pages"
task :deploy_to_user_pages do
  sh "git push user_pages +dinky-theme:master"
end

# ----
#
# Project Pages

desc "Add xxl.git repo as remote"
task :setup_xxl_project_pages do
  sh "git remote add xxl git@github.com:wbzyl/xxl.git"
end

desc "Deploy DINKY THEME to xxl Project Pages"
task :deploy_to_xxl_project_pages do
  sh "git push xxl +dinky-theme:gh-pages"
end

# ----
#
# LESS -> CSS

desc "Compile _less/blog.less to stylesheets/blog.css (requires the less gem)"
task :css do
  sh "lessc _less/blog.less > stylesheets/blog.css"
end

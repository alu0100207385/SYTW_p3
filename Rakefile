desc "Run server"
task :default => :use_keys do
  sh "rackup"
end

desc "Save config.yml out of the CVS"
task :keep_secrets do
  sh "cp config/config_template.yml config/config.yml "
end

desc "Use the filled client_secrets"
task :use_keys do
  sh "cp config/config_filled.yml config/config.yml"
end

desc "Go to console.developers.google"
task :googleconsole do
  sh "gnome-open https://console.developers.google.com/project/corded-observer-516/"
end

desc "Commit changes"
task :ci, [ :message ] => :keep_secrets do |t, args|
  message = args[:message] || ''
  sh "git ci -am '#{message}'"
end

desc "Go to Google security page"
task :revoke do
  sh "gnome-open https://security.google.com/settings/security"
end

desc "Open browser in googles console for this project"
task :googlecredentials do
  sh "gnome-open https://console.developers.google.com/project/corded-observer-516/apiui/credential"
end

desc "Open browser in github repo"
task :my_repo do
  sh "gnome-open https://github.com/alu0100207385"
end

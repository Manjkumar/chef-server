require 'bundler/setup'
require 'omnibus'

Omnibus.setup do |o|
  ##
  # Config Section
  ##
  o.config.install_dir = '/opt/opscode'

  Omnibus::S3Tasks.define!
  Omnibus::CleanTasks.define!
end

Omnibus.projects("config/projects/*.rb")
Omnibus.software("config/software/*.rb")

desc "Print the name and version of all components"
task :versions do
  puts Omnibus::Reports.pretty_version_map
end

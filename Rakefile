$:.push File.expand_path("../lib", __FILE__)
require "familysearch/version"
require 'bundler'
Bundler::GemHelper.install_tasks

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |t|
  t.rspec_opts = "-c"
end
task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = FamilySearch::VERSION

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "familysearch #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

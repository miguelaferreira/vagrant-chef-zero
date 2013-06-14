require 'rake'
require 'rake/testtask'
require 'bundler/setup'

# Immediately sync all stdout so that tools like buildbot can
# immediately load in the output.
$stdout.sync = true
$stderr.sync = true

# Change to the directory of this file.
Dir.chdir(File.expand_path("../", __FILE__))

# This installs the tasks that help with gem creation and
# publishing.
Bundler::GemHelper.install_tasks

# Default task is to run the unit tests
task :default => "test"

Rake::TestTask.new do |t|
  t.pattern = 'spec/**/*_spec.rb'
end
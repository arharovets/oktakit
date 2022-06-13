require "bundler/gem_tasks"

require "rspec/core/rake_task"
RSpec::Core::RakeTask.new(:spec)

require "rubocop/rake_task"
RuboCop::RakeTask.new

task test: :spec
task default: [:spec, :rubocop]

namespace :doc do
  require "yard"
  YARD::Rake::YardocTask.new do |task|
    task.files = ["LICENSE.md", "lib/**/*.rb"]
    task.options = ["--output-dir", "doc/yard", "--markup", "markdown"]
  end
  task default: :yard
end

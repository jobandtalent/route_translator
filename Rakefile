require 'rake'
require 'rake/testtask'
require 'rdoc/task'
require 'rake/bump/tasks'
require 'route_translator/version'

Rake::Bump::Tasks.new(RouteTranslator::VERSION)

desc 'Default: run tests.'
task :default => :test

desc 'Test the translate_routes plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the translate_routes plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'RouteTranslator'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

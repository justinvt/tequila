require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

require 'test/bench'

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the tequila plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.libs << 'test'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end


desc 'Benchmark'
task :bench do
  TequilaBenchmark.run
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    # omitted for brevity
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

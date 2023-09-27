require "rake/testtask"
require "bundler/gem_tasks"
require 'find'

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'List all files'
task :list_files do
  Find.find('.') do |name|
    next if name.include?('/.')
    puts name if File.file?(name)
  end
end

=begin
Add a task to your Rakefile that lists every file in your project except those
whose names begin with . and those that reside in a directory whose name begins with .

You can use Find::find from the Ruby standard library. You will also need
File#file? to test whether a name in Find#find's block is a file or a directory.
=end
require "rake/testtask"
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

desc 'List all files in project'
task :files do 
  Find.find('.') do |file_name| 
    next if file_name.include?('/.')
    puts file_name if File.file?(file_name)
  end
end

##
# Initialise Bundler, catch errors.
##
require 'bundler'
require 'bundler/gem_tasks'

begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts 'Run `bundle install` to install missing gems.'
  exit e.status_code
end

##
# Configure the test suite.
##
require 'rake/testtask'

Rake::TestTask.new :test do |t|
  t.test_files = Dir['test/*_test.rb']
end

##
# By default, just run the tests.
##
task default: :test

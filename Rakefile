# encoding: utf-8

require 'rubygems'
require 'bundler'
require 'jeweler'
require 'rake'
require 'rake/testtask'
require 'rdoc/task'

begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end

Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "pipedrive-ruby"
  gem.homepage = "https://github.com/GeneralScripting/pipedrive-ruby.git"
  gem.license = "MIT"
  gem.summary = %Q{Ruby wrapper for the Pipedrive API}
  gem.description = %Q{Ruby wrapper for the Pipedrive API}
  gem.email = "jan@general-scripting.com"
  gem.authors = ["Jan Schwenzien", "Waldemar Kusnezow", "Joel Courtney"]
  gem.version = File.read('VERSION')
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test

Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "pipedrive-rails #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

require "bundler/gem_tasks"
require "rake/testtask"

Rake::TestTask.new(:test) do |t|
  t.libs << "test/lib"
  t.ruby_opts << "-rhelper"
  t.test_files = FileList['test/**/test_*.rb']
end

ENV['RUBYOPT'] = "-w"

require 'rake/extensiontask'
Rake::ExtensionTask.new("mathn/complex")
Rake::ExtensionTask.new("mathn/rational")

task :default => [:compile, :test]

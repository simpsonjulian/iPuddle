require 'rubygems'
require 'json'
def push(files)
  host = JSON.parse(File.read('hosts.json'))['default'].to_s
  files.each do |file|
    sh "scp #{file} #{host}/"
  end
end
task :default do
 push(['index.html', 'style.css'])
end

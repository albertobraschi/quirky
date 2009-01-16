task :default => :init

desc "Initialise the application"
task :init do
  require 'boot'
  if(!File.exists?(QREPOSITORY_PATH+"/index.yaml"))
    Page.save(
      :name => "index",
      :title => "Congratulations!",
      :content => "h1. You've done it.\n\nYou've installed quirky!",
      :keywords => "amazing, super, awesome",
      :description => "Two words: awesome!"
    )
  else
    puts "Already initialised" 
  end
end

desc "Loads test suite"
task :test do
    QREPOSITORY_PATH = FileUtils.pwd + "/tmp/system"
    require 'boot'
    Dir["tests/**/*.rb"].each { |test| load test }
end
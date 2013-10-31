desc "build"
task :build do
  sh "middleman build"
end

desc "scp to server"
task :push => :build do
  sh "rsync -avr --progress build/* sakura:esolang-book/"
end


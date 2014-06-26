require 'rake'

desc "Parse haml layouts"
task :parse_haml do
  print "Parsing Haml layouts..."
  system(%{
    cd _layouts/haml &&
   for f in *.haml; do [ -e $f ] && haml $f ../${f%.haml}.html; done
  })
  print "Parsing Haml includes..."
  system(%{
    cd _includes/haml &&
    for f in *.haml; do [ -e $f ] && haml $f ../${f%.haml}.html; done
  })
  puts "done."
end

desc "Launch preview environment"
task :preview do
  Rake::Task["parse_haml"].invoke
  system "jekyll serve --watch"
end

desc "Build site"
task :build do |task, args|
  Rake::Task["parse_haml"].invoke
  system "jekyll build"
end

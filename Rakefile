desc 'Delete generated _site files'
task :clean do
  system "rm -fR _site"
end

desc 'Run the jekyll dev server'
task :server do
  system "jekyll --server --auto"
end

desc 'Clean temporary files and run the server'
task :compile => [:clean] do
  system "jekyll"
end

desc 'Publish to krylls.com'
task :publish do
  system "rake compile"
  system "rsync -v -r -c --delete _site/ krylls:/home/public/"
end


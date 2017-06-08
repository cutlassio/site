desc "Deploy site"
task :publish do
  sh "aws s3 sync build/ s3://cutlass.io --cache-control max-age=300"
end

# There's nothing to build yet so we just copy the files. When there is it can be dropped in here.
desc "Build site"
task :build do
  sh "rm -rf ./build"
  sh "cp -r source build"
end

task default: %w[build publish]

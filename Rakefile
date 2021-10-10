abort("Please run this using `bundle exec rake`") unless ENV["BUNDLE_BIN_PATH"]
require "html-proofer"

desc "Build website with jekyll and test with html-proofer"
task :test do
  sh "bundle exec jekyll build"
  options = {
    :allow_hash_href => true,
    :check_html => true,
    :empty_alt_ignore => true,
    :http_status_ignore => [0,400,503,999],
    :internal_domains => ["localhost:4000"],
    :url_ignore => [
      # internal pages
      "/about",
      "/paintings",
      "/photos",
      "/poems",

      # internal posts
      "/i-don't-feel-hungry",
      "/little-things",
      "/potsdam",
      "/three-quarters-of-a-dream",

      # regular expressions
      /poem\/.*/,
      /www\.facebook\.com\/sharer\/.*/,
    ],
    :cache => {
      :timeframe => "6w"
    }
  }
  HTMLProofer.check_directory("./_site/", options).run
end

task :default => [:test]

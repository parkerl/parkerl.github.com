# A sample Guardfile
# More info at https://github.com/guard/guard#readme


require 'guard/guard'
require 'jekyll'

module ::Guard
  class InlineGuard < ::Guard::Guard
    def start
       UI.info "Jekyll waiting for file changes..."
    end
    
    def run_all
      jekyll!
    end
    def run_on_change(paths)
      jekyll!
    end
    
    def jekyll!
      UI.info "Jekyll running."
      
      Jekyll::Site.new(Jekyll.configuration({})).process()

      UI.info "Jekyll complete."
    end
  end
end

guard 'inlineguard' do
  watch(/.*/)
end
# A sample Guardfile
# More info at https://github.com/guard/guard#readme

guard 'spork', :rspec_env => { 'PADRINO_ENV' => 'test' } do
  watch('config/app.rb')
  watch('config/boot.rb')
  watch('config/database.rb')
  watch('Gemfile')
  watch('Gemfile.lock')
  watch('spec/spec_helper.rb') { :rspec }
  watch(%r{^spec/factories/.+\.rb$}) { :rspec }
end

guard 'rspec' do
  watch(%r{^spec/.+_spec\.rb$})
  watch(%r{^app/(.+)\.rb$})           { |m| "spec/app/#{m[1]}_spec.rb" }
  watch(%r{^models/(.+)\.rb$})        { |m| "spec/models/#{m[1]}_spec.rb" }
  watch(%r{^lib/(.+)\.rb$})           { |m| "spec/lib/#{m[1]}_spec.rb" }
  watch(%r{^spec/support/(.+)\.rb$})  { "spec" }
  watch('spec/spec_helper.rb')        { "spec" }
end

# More info at https://github.com/guard/guard#readme
interactor :off

guard 'bundler' do watch('Gemfile') end

# cli: --color --format nested --fail-fast
guard 'rspec', cli: '--drb' do
  watch(%r{^spec/.+_spec\.rb$}) { |m| m[0] }
  # watch(%r{^lib/(.+)\.rb$})     { |m| "spec/lib/#{m[1]}_spec.rb" }`
  watch('spec/spec_helper.rb')  { "spec" }

  watch(%r{^lib/isis/plugins/(.+)\.rb$})                { |m| "spec/plugnis/#{m[1]}_spec.rb" }
  # watch(%r{^app/(.+)\.rb$})                           { |m| "spec/#{m[1]}_spec.rb" }
  # watch(%r{^app/(.*)(\.erb|\.haml)$})                 { |m| "spec/#{m[1]}#{m[2]}_spec.rb" }
  # watch(%r{^app/controllers/(.+)_(controller)\.rb$})  { |m| ["spec/routing/#{m[1]}_routing_spec.rb", "spec/#{m[2]}s/#{m[1]}_#{m[2]}_spec.rb", "spec/acceptance/#{m[1]}_spec.rb"] }
  # watch(%r{^spec/support/(.+)\.rb$})                  { "spec" }
  # watch('config/routes.rb')                           { "spec/routing" }
  # watch('app/controllers/application_controller.rb')  { "spec/controllers" }
end

D = Steep::Diagnostic

target :lib do
  signature "sig"
  check "lib"
  ignore(
    "lib/rbs/prototype/runtime.rb",
    "lib/rbs/test",
    "lib/rbs/test.rb"
  )

  library "set", "pathname", "json", "logger", "monitor", "tsort", "uri", 'yaml', 'dbm', 'pstore', 'singleton', 'shellwords', 'fileutils', 'find', 'digest'
  signature "stdlib/strscan/0/"
  signature "stdlib/rubygems/0/"
  signature "stdlib/optparse/0/"

  configure_code_diagnostics do |config|
    config[D::Ruby::MethodDefinitionMissing] = :hint
    config[D::Ruby::ElseOnExhaustiveCase] = :hint
    config[D::Ruby::FallbackAny] = :hint
  end
end

# target :lib do
#   signature "sig"
#
#   check "lib"                       # Directory name
#   check "Gemfile"                   # File name
#   check "app/models/**/*.rb"        # Glob
#   # ignore "lib/templates/*.rb"
#
#   # library "pathname", "set"       # Standard libraries
#   # library "strong_json"           # Gems
# end

# target :spec do
#   signature "sig", "sig-private"
#
#   check "spec"
#
#   # library "pathname", "set"       # Standard libraries
#   # library "rspec"
# end

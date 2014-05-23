# hammer-cli-import

Tool for importing data from an existing Spacewalk/Satellite system

WORK IN PROGRESS

# Setup info

To enable modules do following:

    mkdir -p ~/.hammer
    cat > ~/.hammer/cli_config.yml << EOF
    :modules:
      - hammer_cli_import
EOF

And running with

    # env RUBYOPT=-Ilib hammer import

To build/install as a gem:

    # gem build hammer_cli_import.gemspec
    # gem install hammer_cli_import-0.0.1.gem
    # hammer import

# Rubocop

Rubocop requires at Ruby 1.9.3. That is in scl.

    # yum install ruby193-ruby-devel
    # scl enable ruby193 bash
    # gem install rubocop

and running with

    # /opt/rh/ruby193/root/usr/local/share/gems/gems/*/bin/rubocop

it should pick up config automatically

# Devel

You can add to your `~/.irbrc`:

    class Object
      def imethods
        methods - Object.instance_methods
      end
    end

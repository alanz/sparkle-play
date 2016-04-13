## Experimenting with building https://github.com/tweag/sparkle out of tree

To use

    $ stack --nix build
    $ stack --nix exec -- mvn -f sparkle -Dsparkle.app=sparkle-example-hello package
    $ stack --nix exec -- spark-submit --master 'local[1]' sparkle/target/sparkle-0.1.jar

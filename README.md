## Experimenting with building https://github.com/tweag/sparkle out of tree

To use

    $ stack --nix build
    # Need the grep in following to get rid of trailing newline
    $ export SPARKLE=`stack --nix query locals sparkle path | grep sparkle`
    $ export SPARKLESRC=$SPARKLE/src/
    $ stack --nix exec -- mvn -f sparkle -Dsparkle.app=sparkle-example-hello -Dsparkle.src=$SPARKLESRC package
    $ stack --nix exec -- spark-submit --master 'local[1]' sparkle/target/sparkle-0.1.jar

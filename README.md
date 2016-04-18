## Experimenting with building https://github.com/tweag/sparkle out of tree

To use

    $ stack --nix build
    $ stack --nix exec sparkle package sparkle-example-hello 
    $ stack --nix exec -- spark-submit --master 'local[1]' sparkle-example-hello.jar

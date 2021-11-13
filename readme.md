## sign and verify using ssh keys

#### create a list of allowed signers from github keys

    $ ./ssh_allowed_signers [github_username ...] | tee ~/.ssh/allowed_signers

#### sign a file using ssh key

    $ ./ssh_sign ~/.ssh/id_ed25519 readme.md

#### verify a file using generated signature

    $ ./ssh_verify ~/.ssh/allowed_signers readme.md.sig readme.md

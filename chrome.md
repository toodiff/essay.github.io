## centos chrome error
$ google-chrome
/usr/bin/google-chrome: symbol lookup error: /usr/bin/google-chrome: undefined symbol: gbm_bo_get_modifier

This is due to a missing symbol in the libgbm library. You will likely need to update the mesa-libgbm package to a later version.
>sudo apt update mesa-libgbm
>sudo yum update mesa-libgbm
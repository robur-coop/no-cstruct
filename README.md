# no-cstruct

This is an opam overlay repository with packages that no longer use cstruct. The reason is that this is quite a big change across the MirageOS ecosystem, and we want to work on it in a distributed way while keeping the same state across installations. Also, adding lots of pin-depends to individual packages / repositories is a lot of work for no obvious good reason (esp. once we update some package, all reverse dependencies need to update their pin-depends).

The plan is to publish all the packages in here to the main opam-repository once we're satisfied and have reviewed the patches.

Using this repository can be done by: `opam repo add no-cstruct git+https://github.com/robur-coop/no-cstruct.git`

Beware, we're also providing a cstruct package which fails to install. This is intentional to avoid accidentally installing any cstruct into a switch. Thus, best to use this repository with a pristine opam switch (`opam switch create no-cstruct 4.14.2` followed by the `opam repo add` from above).

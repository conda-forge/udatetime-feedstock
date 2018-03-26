About udatetime
===============

Home: https://github.com/freach/udatetime

Package license: Apache-2.0

Feedstock license: BSD 3-Clause

Summary: Fast RFC3339 compliant Python date-time library

Handling date-times is a painful act because of the sheer endless amount of formats used by people. Luckily there are a couple of specified standards out there like ISO 8601. But even ISO 8601 leaves to many options on how to define date and time. That\'s why I encourage using the RFC3339 specified date-time format.
udatetime offers on average 76% faster datetime object instantiation, serialization and deserialization of RFC3339 date-time strings. udatetime is using Python\'s datetime class under the hood and code already using datetime should be able to easily switch to udatetime. All datetime objects created by udatetime are timezone-aware. The timezones that udatetime uses are fixed-offset timezones, meaning that they don\'t observe daylight savings time (DST), and thus return a fixed offset from UTC all year round.


Current build status
====================

Linux: [![Circle CI](https://circleci.com/gh/conda-forge/udatetime-feedstock.svg?style=shield)](https://circleci.com/gh/conda-forge/udatetime-feedstock)
OSX: [![TravisCI](https://travis-ci.org/conda-forge/udatetime-feedstock.svg?branch=master)](https://travis-ci.org/conda-forge/udatetime-feedstock)
Windows: ![](https://cdn.rawgit.com/conda-forge/conda-smithy/90845bba35bec53edac7a16638aa4d77217a3713/conda_smithy/static/disabled.svg)

Current release info
====================
Version: [![Anaconda-Server Badge](https://anaconda.org/conda-forge/udatetime/badges/version.svg)](https://anaconda.org/conda-forge/udatetime)
Downloads: [![Anaconda-Server Badge](https://anaconda.org/conda-forge/udatetime/badges/downloads.svg)](https://anaconda.org/conda-forge/udatetime)

Installing udatetime
====================

Installing `udatetime` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `udatetime` can be installed with:

```
conda install udatetime
```

It is possible to list all of the versions of `udatetime` available on your platform with:

```
conda search udatetime --channel conda-forge
```


About conda-forge
=================

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](http://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](http://docs.anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](http://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating udatetime-feedstock
============================

If you would like to improve the udatetime recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/udatetime-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](http://conda.pydata.org/docs/building/meta-yaml.html#build-number-and-string)
   back to 0.
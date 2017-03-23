# Lehigh University Benchmark (LUBM)<br />Artificial Data Generator
The Univ-Bench Artificial Data Generator (UBA) for the Lehigh University Benchmark (LUBM).
This is basically the official code for the generator with some minor tweaks.

## Usage
Requirement for usage is a Java JRE version 5 or higher.
Download a release archive or build the distribution (see `Build` section below).

Usage:

`./bin/dlubm options`

Running without any `options` will print the usage summary.
Note that the default ontology URL usually passed to the `-onto` argument is `http://swat.cse.lehigh.edu/onto/univ-bench.owl`.

## Build
Requirement for building is a Java JDK version 5 or higher and a working Internet connection for the download of dependencies.
[Gradle](https://gradle.org/) is used for build management.

- Build the distribution archives:

`./gradlew clean build assembleDist`

- Build a local distribution:

`./gradlew clean build installDist`

- Change the directory to a local distribution:

`cd build/install/dlubm/`

- Use the local distribution directly:

`./build/install/dlubm/bin/dlubm options`

## Changes

- Code improvements
    - Added `-out <dir>` option to control where generated data files are written
    - Bug fix to use OS specific file separator
- Build management
    - Changed directory structure to be able to build with Gradle
    - Build management via Gradle (see `build` section and `gradle.build` file)
    - Distribution building via Gradle (see `build` section and `gradle.build` file)
    - Launch scripts generated by Gradle
    - Configuration for GitLab CI

## Copyright / Contact

### Gradle Integration

- Felix Leif Keppmann <felix.leif@keppmann.de>

### Improved Version

- Rob Vesse <rvesse@dotnetrdf.org>
- For more information on the improved version, visit [https://github.com/rvesse/lubm-uba](https://github.com/rvesse/lubm-uba)

### Original Version

- The Semantic Web and Agent Technologies (SWAT) Lab, CSE Department, Lehigh University
- Yuanbo Guo <yug2@lehigh.edu>
- For more information about the benchmark, visit [http://swat.cse.lehigh.edu/projects/lubm](http://swat.cse.lehigh.edu/projects/lubm)
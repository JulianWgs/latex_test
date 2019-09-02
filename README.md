# latex_test
Test repository for compiling LaTex documents in the cloud

## Tutorial

Two things need to be set up. First the files in the repository and second the integration with Travis CI (the cloud build platform).

### The files

- The main.tex file is an ordinary `.tex`-file and can also be compiled into a pdf offline

- The second needed file is the `.travis.yml`. In that file the build script is defined. 

  1. Dependencies are being  installed

  2. The Latex-File is compiled

  3. A release is packaged and uploaded to github. The command `travis setup releases` sets everything up safely. Just follow the instructions. Installation instruction for travis can be found [here](https://github.com/travis-ci/travis.rb#installation). Also add these flags to only run on tagged commits and don't delete build artifacts.

     ```yaml
     skip_cleanup: true
     on:
         tags: true
     ```

### Travis CI

Travis CI is a build platform which is free for open source projects. It is possible to login there via the github account. A tutorial can be found [here](https://github.com/mbonaci/mbo-storm/wiki/Integrate-Travis-CI-with-your-GitHub-repo).

I will publish more info when Im back from Denmark :)
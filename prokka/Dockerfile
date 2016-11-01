FROM linuxbrew/linuxbrew
MAINTAINER Shaun Jackman <sjackman@gmail.com>

RUN sudo apt-get install --yes --no-install-recommends bioperl libxml-simple-perl

RUN brew tap homebrew/science

# Install infernal before hmmer to avoid this error:
# exactmatch.c: undefined reference to `fm_getChar'
RUN brew install infernal -v

RUN brew install --only-dependencies prokka -v
RUN brew install prokka -v

ENTRYPOINT ["prokka"]

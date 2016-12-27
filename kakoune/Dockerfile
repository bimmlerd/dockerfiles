FROM alpine:latest
MAINTAINER David Bimmler <david.bimmler@infix.ch>

# Install build requirements.
RUN apk add --no-cache \
	build-base \
	git \
	ncurses-dev \
	boost-dev \
	asciidoc

# Build and install kakoune.
RUN git clone https://github.com/mawww/kakoune /src/kakoune
WORKDIR /src/kakoune/src
RUN make && make install

ENTRYPOINT ["kak"]



FROM gcc as builder

WORKDIR /

ADD https://github.com/wg/wrk/archive/4.1.0.tar.gz .
RUN tar xvf 4.1.0.tar.gz && \
    cd wrk-4.1.0 && \
    make

FROM fedora:29

LABEL maintainer="gopher.mian@outlook.com"

WORKDIR /workspace

COPY --from=builder /wrk-4.1.0/wrk .

ENTRYPOINT ["./wrk"]

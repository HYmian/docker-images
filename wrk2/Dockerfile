FROM gcc as builder

WORKDIR /

RUN git clone https://github.com/giltene/wrk2.git && \
    cd wrk2 && \
    make

FROM debian:buster

LABEL maintainer="gopher.mian@outlook.com"

WORKDIR /workspace

COPY --from=builder /wrk2/wrk /workspace

ENTRYPOINT ["/workspace/wrk"]

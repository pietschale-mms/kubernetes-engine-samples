FROM golang:1.8-alpine
ADD main.go /go/src/hello-app
RUN cd /go/src/hello-app
RUN go install

FROM alpine:latest
COPY --from=0 /go/bin/hello-app .
ENV PORT 8080
CMD ["./hello-app"]

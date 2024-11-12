FROM golang AS executavel
ENV GO111MODULE=auto
WORKDIR /go/src/app
COPY app.go /go/src/app/
RUN go build -o app .

FROM alpine
WORKDIR /appexec
COPY --from=executavel /go/src/app /appexec/
RUN chmod -R 755 /appexec
ENTRYPOINT ["./app"]

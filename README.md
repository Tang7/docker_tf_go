## Dockerfile to create image contains tensorflow-go and golang.

> Note: Current Dockerfile is alread built and published as hopipola/tf_go

* ### Verify the image and use it:

1. Create a Dockerfile in the same path of test_tf.go:
```
FROM hopipola/tf_go

WORKDIR /go/src/hello_tf

COPY . .

RUN go build

ENTRYPOINT [ "/go/src/hello_tf/hello_tf" 
```
2. Build a local docker image
```
docker build -t imageName .
```

3. Run the image to verify tensorflow and go are install sccuessfully:
```
docker run imageName
```

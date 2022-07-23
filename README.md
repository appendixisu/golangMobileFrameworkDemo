# golangMobileFrameworkDemo

This is a golang to mobile application framework demo using gomobile.

## Environment

### Install ```GO```

```sh
$ brew install go
>
```

### Install ```gomobile```

```sh
 $ go install golang.org/x/mobile/cmd/gomobile@latest
 >
 $ gomobile init
 >
```

## Write GO

### Step1. Create Go Module

```sh
mkdir golangMobileFrameworkDemo
cd golangMobileFrameworkDemo
go mod init verification
```

### Step2. Create Go File ```verification.go```

For content, please refer to git file.

### Step3. Ensure that all imports are satisfied

```sh
go mod tidy
```

### Step4. add `github.com/ydnar/gomobile` to `go.mod`

`github.com/ydnar/gomobile` is a 3rd party gomobile supporting Apple Silicon

```go
replace golang.org/x/mobile v0.0.0-20210614202936-7c8f154d1008 => github.com/ydnar/gomobile v0.0.0-20210301201239-fb6ffafc9ef9
```

### Step5. setting gomobile

``` sh
go get golang.org/x/mobile/cmd/gomobile
go get golang.org/x/mobile/bind
```

### Step6. build to XCFramework for iOS

```sh
gomobile bind -target ios -o Sources/Verification.xcframework .
```


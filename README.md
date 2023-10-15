# simple-cron
Library to run func by cron. Also to limit func runtime. Written in Golang

## install

```bash
go get github.com/Sagleft/cronlib
```

### usage example

```go
var myfunc = func() {
	// func example
	time.Sleep(time.Second * 10)
}

isTimeIsUP := simplecron.NewRuntimeLimitHandler(
	time.Second * 2,
	myfunc,
).Run()
if isTimeIsUP {
	// handle timeout
}
```

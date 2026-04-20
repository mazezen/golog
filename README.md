## golog

> use zap logger

```bash
go get -u github.com/mazezen/golog@latest
```

### usage

```go
type User struct {Name string; Url string}
u := []struct{Name string; Url string}{{ Name: "go", Url: "go.dev" }}

NewLogger(
	WithLoggerFilePath("./app.log"),
	WithLoggerConsole(false),
	WithLoggerFormatter("json"),
)

Logger.Debug("test debug ...", zap.Any("user", u))
Logger.Info("test debug ...", zap.Any("user", u))
Logger.Warn("test debug ...", zap.Any("user", u))
Logger.Error("test debug ...", zap.Any("user", u))



Logger.SugarDebug("test sugar ..")
Logger.SugarDebugf("test sugar u = %v", u)
Logger.SugarDebugw("test sugar u", "user", u)

Logger.SugarInfo("test sugar ..")
Logger.SugarInfof("test sugar u = %v", u)
Logger.SugarInfow("test sugar u", "user", u)

Logger.SugarWarn("test sugar ..")
Logger.SugarWarnf("test sugar u = %v", u)
Logger.SugarWarnw("test sugar u", "user", u)

Logger.SugarError("test sugar ..")
Logger.SugarErrorf("test sugar u = %v", u)
Logger.SugarErrorw("test sugar u", "user", u)

Logger.SugarDPanic("test sugar ..")
Logger.SugarDPanicf("test sugar u = %v", u)
Logger.SugarDPanicw("test sugar u", "user", u)
```

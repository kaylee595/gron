# gron
主要是修复时间不正确问题, 官方的版本提了`pull request`但是不修复.<br>
The main thing is to fix the incorrect time problem, the official version mentions `pull request` but doesn't fix it.<br>
```golang
func (as atSchedule) reset(t time.Time) time.Time {
	return time.Date(t.Year(), t.Month(), t.Day(), as.hh, as.mm, 0, 0, time.Local)  // 将time.UTC修改为time.Local. (Change time.UTC to time.Local.)
}
```
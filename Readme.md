# 使用OpenCensus（体验版）

1. 下载Prometheus：
```
wget https://github.com/prometheus/prometheus/releases/download/v2.18.1/prometheus-2.18.1.darwin-amd64.tar.gz
``` 
或者前往https://prometheus.io/download/ 用浏览器下载  
2. 进入存储prometheus压缩包的目录，比如: `~/Downloads`
```
cd <prometheus-2.18.1.darwin-amd64.tar.gz 的下载目录>, 
比如这里是：cd ~/Downloads
```
3. 执行如下命令解压：
```
tar xvfz prometheus-*.tar.gz
```
4. 在IDE中通过Git URL： https://github.com/lisz1012/quickstart.git 创建新项目
5. 命令行中执行下面的命令启动 prometheus，以对程序开启监控：
```
~/Downloads/prometheus-2.18.1.darwin-amd64/prometheus --config.file=promconfig.yaml
```
6. 前往 http://localhost:9090 （这里是9090端口，因为在prometheus的配置文件：promconfig.yaml中配置了）查看 UI 和 Graph，如：
   http://localhost:9090/graph?g0.range_input=5m&g0.expr=ocjavametrics_latency_bucket&g0.tab=0
7. 执行io.opencensus.metrics.quickstart.Repl.java 中的 main 方法，输入一些字符串并回车
8. 刷新网页查看图表的变化

### 参考链接
https://opencensus.io/quickstart/java/metrics/#0  
https://prometheus.io/docs/prometheus/latest/getting_started/  
https://prometheus.io/download/
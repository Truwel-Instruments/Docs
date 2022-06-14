<h1 id="header">
    <center>
</h1>

###### SDI12地址初始为'0'，命令可以地址'0'或者'?'开头，命令可以全部大写或全部小写
 
#### 模式一（PSW模式，默认模式）
###### 适用于只接入PSW传感器场景
```
sdi12 recorder command -> "0CONFIG PSW MODE!"
sdi12 sensor response  -> "0PSW MODE\r\n"
```
###### 模式一下，SDI12命令及相应	
```
sdi12 recorder command -> "0M!"
sdi12 sensor response  -> "00001\r\n"
```
```
sdi12 recorder command -> "0D0!"
sdi12 sensor response  -> "0+PSW\r\n"
```
#### 模式二（PLL模式）
###### 适用于只接入PLL传感器场景
```
sdi12 recorder command -> "0CONFIG PLL MODE!"
sdi12 sensor response  -> "0PLL MODE\r\n"
```
###### 模式二下，SDI12命令及相应	
```
sdi12 recorder command -> "0M!"
sdi12 sensor response  -> "00001\r\n"
```
```
sdi12 recorder command -> "0D0!"
sdi12 sensor response  -> "0+PLL\r\n"
```
#### 模式三（PSW、PLL自由选择模式）
###### 适用于同时接入PSW和PLL传感器的场景
```
sdi12 recorder command -> "0CONFIG DUAL MODE!"
sdi12 sensor response  -> "0FREE MODE\r\n"
```
###### 模式三下，SDI12命令及相应	
```
sdi12 recorder command -> "0M!"
sdi12 sensor response  -> "00002\r\n"
```
```
sdi12 recorder command -> "0D0!"
sdi12 sensor response  -> "0+PSW+PLL\r\n"
```	
#### 任意模式下

```
sdi12 recorder command -> "0M0!"
sdi12 sensor response  -> "00001\r\n"
```
```
sdi12 recorder command -> "0D0!"
sdi12 sensor response  -> "0+PSW\r\n"
```	
```
sdi12 recorder command -> "0M1!"
sdi12 sensor response  -> "00001\r\n"
```
```
sdi12 recorder command -> "0D0!"
sdi12 sensor response  -> "0+PLL\r\n"
```
```
sdi12 recorder command -> "0M2!"
sdi12 sensor response  -> "00002\r\n"
```
```
sdi12 recorder command -> "0D0!"
sdi12 sensor response  -> "0+PSW+PLL\r\n"
```
#### 系数设定
###### 设定PSW倍乘示例
```
sdi12 recorder command -> "0CONFIG PSW GAIN 1.0!"
sdi12 sensor response  -> "0PSW GAIN 1.0\r\n"
```
###### 设定PSW偏移量示例
```
sdi12 recorder command -> "0CONFIG PSW OFFSEET 0.2!"
sdi12 sensor response  -> "0PSW OFFSEET 0.2\r\n"
```
###### 设定PLL倍乘示例
```
sdi12 recorder command -> "0CONFIG PLL GAIN 1.0!"
sdi12 sensor response  -> "0PLL GAIN 1.0\r\n"
```
###### 设定PLL倍乘示例
```
sdi12 recorder command -> "0CONFIG PLL OFFSEET 0.2!"
sdi12 sensor response  -> "0PLL OFFSEET 0.2\r\n"
```
#### 查询配置
```
sdi12 recorder command -> "0HELP!"
sdi12 sensor response  ->
PSW MODE
PSW GAIN =1.0
PSW OFFSET =0.0
PLL GAIN =1.0
PLL OFFSET =0.0
"
```

<a href="#header">回到顶部</a>
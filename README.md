对于一个字幕文本本身没有大问题的字幕文件来进行规则校验


1. 业务痛点
a. 手动校验：工作人员需要手动进行
b. 迭代周期长：当前百草/若谷，均有自己独立的筛稿引擎，当新增/下线特征时，不支持动态配置生效，需要编码上线
c. 执行效率低：目前已有的规则处理流程是串行执行的，执行效率低


开发的优先级：
1. 位置规则
2. 长度规则
3. 大小规则
4. 颜色规则
5. 其他规则

定义规则树、配置变量、规则预加载

规则集的执行单元

解析完成字幕文件和其他文件之后，并行对字幕块进行校验



1. 加载自定义规则配置文件，如没有，则采用默认规则
2. 加载字幕文件以及相关资源文件
3. 解析文件，并行规则处理
4. 归并处理相邻字幕块，颜色防抖处理



此模块将sparrow项目的各个子模块合并成一个jar 其中包含了各个模块中的包和类
修改注意：

1) 添加了新的模块，要在POM中maven-shade-plugin的<artifactSet>中添加<include>

2) 添加了新的扩展点，要在POM中maven-shade-plugin加上<transformer>

搜索出 扩展点配置文件 的命令

$ find . -wholename */META-INF/sparrow/* -type f | grep -vF /test/ | awk -F/ '{print $NF}' | sort -u
com.dynamo.sparrow.cache.CacheFactory
com.dynamo.sparrow.common.compiler.Compiler
com.dynamo.sparrow.common.extension.ExtensionFactory
...and so on...

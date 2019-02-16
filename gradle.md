### 调试gradle脚本
首先将需要调试的代码引入当前工程dependencies DSL中
```
dependencies {
    gradleApi()
    localGroovy()
    implementation('io.spring.gradle:dependency-management-plugin:1.0.6.RELEASE')
}
```
如果工程的依赖中出现了这些类，在命令行中执行
```
gradlew <task> -Dorg.gradle.debug=true --no-daemon
```
最后新建Intellij IDEA的remote debug进行调试，端口号填5005，debug开始

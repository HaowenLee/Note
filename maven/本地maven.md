# 本地maven

# ## 在module的build.gradle里添加：

```
apply plugin: 'maven'

uploadArchives {
    repositories.mavenDeployer {
        // 配置本地仓库路径，项目根目录下的repository目录中
        repository(url: uri('../repository'))
        pom.groupId = "com.haowen.huge"// 唯一标识（通常为模块包名，也可以任意）
        pom.artifactId = "huge-annotations" // 项目名称（通常为类库模块名称，也可以任意）
        pom.version = "1.0.0" // 版本号
    }
}
```



## 点击Gradle-upload-uploadArchives任务：

## 在project的build.gradle里添加仓库的地址：

```
//本地Maven仓库地址
maven {
    url 'file://C://Users//Li//AndroidStudioProjects//huge//repository'
}
```
# 环境支持

## idea支持jdk17

1. Projects settings 设置为 jdk17

   ![image-20240810172923455](https://biliww.github.io/imgs/md/202408101729897.png)

2. Gradle 配置jdk17版本

   ![image-20240810173104248](https://biliww.github.io/imgs/md/202408101731286.png)



## gradle仓库环境配置

1. 直接梯子无需更改任何配置
2. setting.gradle配置文件

```
pluginManagement {
    repositories {
        maven { url 'https://repo.spring.io/milestone' }
        gradlePluginPortal()
    }
}

rootProject.name = 'halo'
include 'api', 'application', 'platform:application', 'platform:plugin', 'ui'

```

http://mirrors.cloud.tencent.com/

## 构建

![image-20240810172955512](https://biliww.github.io/imgs/md/202408101729550.png)



构建过程：

```
Download https://services.gradle.org/distributions/gradle-8.8-bin.zip, took 2 m 36 s 783 ms (138.04 MB)
Starting Gradle Daemon...
Gradle Daemon started in 838 ms
> Task :buildSrc:extractPluginRequests UP-TO-DATE
> Task :buildSrc:generatePluginAdapters UP-TO-DATE
> Task :buildSrc:compileJava
> Task :buildSrc:compileGroovy NO-SOURCE
> Task :buildSrc:compileGroovyPlugins
> Task :buildSrc:pluginDescriptors UP-TO-DATE
> Task :buildSrc:processResources UP-TO-DATE
> Task :buildSrc:classes
> Task :buildSrc:jar
Download https://plugins.gradle.org/m2/org/springframework/boot/spring-boot-gradle-plugin/3.3.1/spring-boot-gradle-plugin-3.3.1.pom, took 1 s 430 ms (2.85 kB)
Download https://plugins.gradle.org/m2/org/springframework/boot/spring-boot-gradle-plugin/3.3.1/spring-boot-gradle-plugin-3.3.1.module, took 497 ms (10.53 kB)
Download https://plugins.gradle.org/m2/io/spring/gradle/dependency-management-plugin/1.1.5/dependency-management-plugin-1.1.5.pom, took 1 s 331 ms (1.73 kB)
Download https://plugins.gradle.org/m2/io/spring/gradle/dependency-management-plugin/1.1.5/dependency-management-plugin-1.1.5.module, took 499 ms (3.63 kB)
Download https://plugins.gradle.org/m2/com/gorylenko/gradle-git-properties/gradle-git-properties/2.4.1/gradle-git-properties-2.4.1.module, took 666 ms (1.94 kB)
Download https://plugins.gradle.org/m2/de/undercouch/gradle-download-task/5.6.0/gradle-download-task-5.6.0.pom, took 426 ms (1.7 kB)
Download https://plugins.gradle.org/m2/de/undercouch/gradle-download-task/5.6.0/gradle-download-task-5.6.0.module, took 1 s 363 ms (2.7 kB)
Download https://plugins.gradle.org/m2/io/freefair/gradle/lombok-plugin/8.6/lombok-plugin-8.6.pom, took 424 ms (2.17 kB)
Download https://plugins.gradle.org/m2/io/freefair/gradle/lombok-plugin/8.6/lombok-plugin-8.6.module, took 525 ms (3.47 kB)
Download https://plugins.gradle.org/m2/com/github/node-gradle/gradle-node-plugin/7.0.2/gradle-node-plugin-7.0.2.module, took 1 s 389 ms (3.97 kB)
Download https://plugins.gradle.org/m2/org/springdoc/springdoc-openapi-gradle-plugin/1.9.0/springdoc-openapi-gradle-plugin-1.9.0.pom, took 522 ms (1.94 kB)
Download https://plugins.gradle.org/m2/org/springdoc/springdoc-openapi-gradle-plugin/1.9.0/springdoc-openapi-gradle-plugin-1.9.0.module, took 552 ms (5.13 kB)
Download https://plugins.gradle.org/m2/org/springframework/spring-core/6.1.10/spring-core-6.1.10.pom, took 774 ms (2.03 kB)
Download https://plugins.gradle.org/m2/org/springframework/spring-core/6.1.10/spring-core-6.1.10.module, took 261 ms (2.52 kB)
Download https://plugins.gradle.org/m2/org/apache/commons/commons-compress/1.25.0/commons-compress-1.25.0.pom, took 352 ms (21.7 kB)
Download https://plugins.gradle.org/m2/org/springframework/boot/spring-boot-buildpack-platform/3.3.1/spring-boot-buildpack-platform-3.3.1.pom, took 526 ms (3.21 kB)
Download https://plugins.gradle.org/m2/org/springframework/boot/spring-boot-loader-tools/3.3.1/spring-boot-loader-tools-3.3.1.pom, took 558 ms (2.24 kB)
Download https://plugins.gradle.org/m2/org/apache/commons/commons-parent/64/commons-parent-64.pom, took 259 ms (77.96 kB)
Download https://plugins.gradle.org/m2/org/apache/apache/30/apache-30.pom, took 221 ms (23.24 kB)
Download https://plugins.gradle.org/m2/org/springframework/boot/spring-boot-buildpack-platform/3.3.1/spring-boot-buildpack-platform-3.3.1.module, took 1 s 74 ms (8.23 kB)
Download https://plugins.gradle.org/m2/org/springframework/boot/spring-boot-loader-tools/3.3.1/spring-boot-loader-tools-3.3.1.module, took 1 s 72 ms (6.41 kB)
Download https://plugins.gradle.org/m2/org/junit/junit-bom/5.10.0/junit-bom-5.10.0.pom, took 201 ms (5.65 kB)
Download https://plugins.gradle.org/m2/org/junit/junit-bom/5.10.0/junit-bom-5.10.0.module, took 179 ms (7 kB)
Download https://plugins.gradle.org/m2/com/google/guava/guava/31.0.1-jre/guava-31.0.1-jre.pom, took 186 ms (10.96 kB)
Download https://plugins.gradle.org/m2/com/google/guava/guava-parent/31.0.1-jre/guava-parent-31.0.1-jre.pom, took 194 ms (13.83 kB)
Download https://plugins.gradle.org/m2/com/fasterxml/jackson/core/jackson-databind/2.14.2/jackson-databind-2.14.2.module, took 170 ms (3.22 kB)
Download https://plugins.gradle.org/m2/org/awaitility/awaitility-kotlin/4.0.3/awaitility-kotlin-4.0.3.pom, took 196 ms (4.48 kB)
Download https://plugins.gradle.org/m2/com/google/code/gson/gson/2.8.9/gson-2.8.9.pom, took 205 ms (6.33 kB)
Download https://plugins.gradle.org/m2/com/google/code/gson/gson-parent/2.8.9/gson-parent-2.8.9.pom, took 175 ms (4.68 kB)
Download https://plugins.gradle.org/m2/org/jetbrains/kotlin/kotlin-stdlib-jdk8/1.8.20/kotlin-stdlib-jdk8-1.8.20.pom, took 945 ms (1.58 kB)
Download https://plugins.gradle.org/m2/org/jetbrains/kotlin/kotlin-reflect/1.8.20/kotlin-reflect-1.8.20.pom, took 245 ms (1.38 kB)
Download https://plugins.gradle.org/m2/org/awaitility/awaitility-parent/4.0.3/awaitility-parent-4.0.3.pom, took 1 s 75 ms (10.26 kB)
Download https://plugins.gradle.org/m2/com/github/psxpaul/gradle-execfork-plugin/0.2.0/gradle-execfork-plugin-0.2.0.pom, took 1 s 778 ms (1.18 kB)
Download https://plugins.gradle.org/m2/com/github/psxpaul/gradle-execfork-plugin/0.2.0/gradle-execfork-plugin-0.2.0.module, took 1 s 398 ms (2.54 kB)
Download https://plugins.gradle.org/m2/net/java/dev/jna/jna-platform/5.13.0/jna-platform-5.13.0.pom, took 171 ms (2.25 kB)
Download https://plugins.gradle.org/m2/org/apache/httpcomponents/client5/httpclient5/5.3.1/httpclient5-5.3.1.pom, took 186 ms (5.96 kB)
Download https://plugins.gradle.org/m2/org/apache/httpcomponents/client5/httpclient5-parent/5.3.1/httpclient5-parent-5.3.1.pom, took 183 ms (16.68 kB)
Download https://plugins.gradle.org/m2/com/fasterxml/jackson/module/jackson-module-parameter-names/2.14.2/jackson-module-parameter-names-2.14.2.module, took 159 ms (3.28 kB)
Download https://plugins.gradle.org/m2/org/junit/junit-bom/5.10.1/junit-bom-5.10.1.pom, took 178 ms (5.65 kB)
Download https://plugins.gradle.org/m2/org/junit/junit-bom/5.10.1/junit-bom-5.10.1.module, took 177 ms (7 kB)
Download https://plugins.gradle.org/m2/org/springframework/spring-jcl/6.1.10/spring-jcl-6.1.10.pom, took 1 s 158 ms (1.85 kB)
Download https://plugins.gradle.org/m2/org/springframework/spring-jcl/6.1.10/spring-jcl-6.1.10.module, took 1 s 72 ms (1.9 kB)
Download https://plugins.gradle.org/m2/org/checkerframework/checker-qual/3.12.0/checker-qual-3.12.0.pom, took 185 ms (2.09 kB)
Download https://plugins.gradle.org/m2/org/checkerframework/checker-qual/3.12.0/checker-qual-3.12.0.module, took 179 ms (3.55 kB)
Download https://plugins.gradle.org/m2/com/google/errorprone/error_prone_annotations/2.7.1/error_prone_annotations-2.7.1.pom, took 432 ms (2.11 kB)
Download https://plugins.gradle.org/m2/com/google/errorprone/error_prone_parent/2.7.1/error_prone_parent-2.7.1.pom, took 192 ms (6.98 kB)
Download https://plugins.gradle.org/m2/com/fasterxml/jackson/core/jackson-annotations/2.14.2/jackson-annotations-2.14.2.module, took 163 ms (2.53 kB)
Download https://plugins.gradle.org/m2/com/fasterxml/jackson/core/jackson-core/2.14.2/jackson-core-2.14.2.module, took 161 ms (2.49 kB)
Download https://plugins.gradle.org/m2/org/jetbrains/kotlin/kotlin-stdlib/1.8.20/kotlin-stdlib-1.8.20.pom, took 1 s 140 ms (1.55 kB)
Download https://plugins.gradle.org/m2/org/awaitility/awaitility/4.0.3/awaitility-4.0.3.pom, took 190 ms (3.55 kB)
Download https://plugins.gradle.org/m2/org/jetbrains/kotlin/kotlin-stdlib-jdk7/1.8.20/kotlin-stdlib-jdk7-1.8.20.pom, took 1 s 78 ms (1.39 kB)
Download https://plugins.gradle.org/m2/net/java/dev/jna/jna/5.13.0/jna-5.13.0.pom, took 170 ms (2.03 kB)
Download https://plugins.gradle.org/m2/org/apache/httpcomponents/core5/httpcore5/5.2.4/httpcore5-5.2.4.pom, took 208 ms (3.95 kB)
Download https://plugins.gradle.org/m2/org/apache/httpcomponents/core5/httpcore5-h2/5.2.4/httpcore5-h2-5.2.4.pom, took 285 ms (3.62 kB)
Download https://plugins.gradle.org/m2/org/apache/httpcomponents/core5/httpcore5-parent/5.2.4/httpcore5-parent-5.2.4.pom, took 193 ms (13.72 kB)
Download https://plugins.gradle.org/m2/org/junit/junit-bom/5.9.3/junit-bom-5.9.3.module, took 182 ms (6.96 kB)
Download https://plugins.gradle.org/m2/org/jetbrains/kotlin/kotlin-stdlib-common/1.8.20/kotlin-stdlib-common-1.8.20.pom, took 1 s 128 ms (1.16 kB)
Download https://plugins.gradle.org/m2/org/hamcrest/hamcrest/2.1/hamcrest-2.1.pom, took 166 ms (1.13 kB)
Download https://plugins.gradle.org/m2/gradle/plugin/org/gradle/crypto/checksum/1.4.0/checksum-1.4.0.jar, took 193 ms (8.76 kB)
Download https://plugins.gradle.org/m2/org/springdoc/springdoc-openapi-gradle-plugin/1.9.0/springdoc-openapi-gradle-plugin-1.9.0.jar, took 359 ms (28.84 kB)
Download https://plugins.gradle.org/m2/org/springframework/boot/spring-boot-loader-tools/3.3.1/spring-boot-loader-tools-3.3.1.jar, took 485 ms (458.44 kB)
Download https://plugins.gradle.org/m2/io/freefair/gradle/lombok-plugin/8.6/lombok-plugin-8.6.jar, took 611 ms (41.38 kB)

```

等待一段时间出现：

```bash
Deprecated Gradle features were used in this build, making it incompatible with Gradle 9.0.

You can use '--warning-mode all' to show the individual deprecation warnings and determine if they come from your own scripts or plugins.

For more on this, please refer to https://docs.gradle.org/8.8/userguide/command_line_interface.html#sec:command_line_warnings in the Gradle documentation.

BUILD SUCCESSFUL in 6m 43s
7 actionable tasks: 3 executed, 4 up-to-date

```

## 运行

### 服务端启动

![image-20240810173907257](https://biliww.github.io/imgs/md/202408101739299.png)



```java
> Task :application:Application.main()

    __  __      __
   / / / /___ _/ /___
  / /_/ / __ `/ / __ \
 / __  / /_/ / / /_/ /
/_/ /_/\__,_/_/\____/

Version: 
2024-08-10T17:39:34.674+08:00  INFO 13996 --- [           main] run.halo.app.Application                 : Starting Application using Java 17.0.11 with PID 13996 (/Users/wangpenglong/ideaProject/githubStudy/haloGithub/application/build/classes/java/main started by wangpenglong in /Users/wangpenglong/ideaProject/githubStudy/haloGithub)
2024-08-10T17:39:34.675+08:00 DEBUG 13996 --- [           main] run.halo.app.Application                 : Running with Spring Boot v3.3.1, Spring v6.1.10
2024-08-10T17:39:34.676+08:00  INFO 13996 --- [           main] run.halo.app.Application                 : The following 1 profile is active: "dev"
2024-08-10T17:39:34.773+08:00  WARN 13996 --- [           main] o.s.c.a.AnnotationBeanNameGenerator      : Support for convention-based stereotype names is deprecated and will be removed in a future version of the framework. Please annotate the 'value' attribute in @run.halo.app.theme.finders.Finder with @AliasFor(annotation=Component.class) to declare an explicit alias for @Component's 'value' attribute.
2024-08-10T17:39:35.356+08:00  INFO 13996 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Multiple Spring Data modules found, entering strict repository configuration mode
2024-08-10T17:39:35.357+08:00  INFO 13996 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data R2DBC repositories in DEFAULT mode.
2024-08-10T17:39:35.450+08:00  INFO 13996 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 86 ms. Found 1 R2DBC repository interface.
2024-08-10T17:39:37.171+08:00  INFO 13996 --- [           main] o.s.b.a.e.web.EndpointLinksResolver      : Exposing 34 endpoints beneath base path '/actuator'
2024-08-10T17:39:37.279+08:00  INFO 13996 --- [           main] org.pf4j.DefaultPluginStatusProvider     : Enabled plugins: []
2024-08-10T17:39:37.280+08:00  INFO 13996 --- [           main] org.pf4j.DefaultPluginStatusProvider     : Disabled plugins: []
2024-08-10T17:39:37.281+08:00  INFO 13996 --- [           main] org.pf4j.DefaultPluginManager            : PF4J version 3.12.0 in 'development' mode
2024-08-10T17:39:37.320+08:00  INFO 13996 --- [           main] r.h.a.s.a.impl.RsaKeyService             : Generating RSA keys for PAT.
2024-08-10T17:39:39.681+08:00  INFO 13996 --- [           main] r.h.a.s.a.impl.RsaKeyService             : Wrote RSA keys for PAT into /Users/wangpenglong/halo2-dev/keys/pat_id_rsa and /Users/wangpenglong/halo2-dev/keys/pat_id_rsa.pub
2024-08-10T17:39:40.503+08:00 DEBUG 13996 --- [           main] run.halo.app.console.ProxyFilter         : Initialized ProxyFilter to proxy /console/** to endpoint http://localhost:3000/
2024-08-10T17:39:40.505+08:00 DEBUG 13996 --- [           main] run.halo.app.console.ProxyFilter         : Initialized ProxyFilter to proxy /uc/** to endpoint http://localhost:4000/
2024-08-10T17:39:40.708+08:00  INFO 13996 --- [           main] r.h.a.search.lucene.LuceneSearchEngine   : Initialized lucene search engine
2024-08-10T17:39:41.441+08:00  INFO 13996 --- [           main] o.s.b.web.embedded.netty.NettyWebServer  : Netty started on port 8090 (http)
```

Netty started on port 8090 (http)出现代表运行成功

### 前端启动

#### 前提条件：

- [Node.js 20 LTS](https://nodejs.org/)
- [pnpm 9](https://pnpm.io/)

```bash
cd path/to/halo/ui
pnpm install
pnpm build:packages
pnpm dev
```

```bash
Scope: all 6 workspace projects
Lockfile is up to date, resolution step is skipped
Packages: +2242
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Downloading @iconify/json@2.2.147: 67.91 MB/67.91 MB, done
Progress: resolved 2242, reused 1714, downloaded 487, added 2242, done
node_modules/.pnpm/esbuild@0.20.2/node_modules/esbuild: Running postinstall script, done in 559ms
node_modules/.pnpm/esbuild@0.17.19/node_modules/esbuild: Running postinstall script, done in 311ms
node_modules/.pnpm/vue-demi@0.14.7_vue@3.4.27_typescript@5.3.3_/node_modules/vue-demi: Running postinstall script, done in 83ms
node_modules/.pnpm/vue-demi@0.13.11_vue@3.4.27_typescript@5.3.3_/node_modules/vue-demi: Running postinstall script, done in 74ms
node_modules/.pnpm/cypress@10.11.0/node_modules/cypress: Running postinstall script, done in 2m 54.9s
node_modules/.pnpm/@nestjs+core@10.3.0_@nestjs+common@10.3.0_reflect-metadata@0.1.13_rxjs@7.8.1__reflect-metadata@0.1.13_rxjs@7.8.1/node_modules/@nestjs/core: Running postinstall script, done in 1.1s
node_modules/.pnpm/esbuild@0.14.54/node_modules/esbuild: Running postinstall script, done in 986ms
node_modules/.pnpm/esbuild@0.18.20/node_modules/esbuild: Running postinstall script, done in 1s
node_modules/.pnpm/@openapitools+openapi-generator-cli@2.13.4/node_modules/@openapitools/openapi-generator-cli: Running postinstall script, done in 1.6s

dependencies:
+ @codemirror/commands 6.1.2
+ @codemirror/lang-css 6.0.1
+ @codemirror/lang-html 6.2.0
+ @codemirror/lang-javascript 6.1.1
+ @codemirror/lang-json 6.0.1
+ @codemirror/language 6.3.1
+ @codemirror/legacy-modes 6.3.0
+ @codemirror/state 6.1.4
+ @codemirror/view 6.5.1
+ @emoji-mart/data 1.2.1
+ @formkit/core 1.5.9
+ @formkit/i18n 1.5.9
+ @formkit/inputs 1.5.9
+ @formkit/themes 1.5.9
+ @formkit/utils 1.5.9
+ @formkit/validation 1.5.9
+ @formkit/vue 1.5.9
+ @tanstack/vue-query 4.29.1
+ @tiptap/extension-character-count 2.5.7
+ @uppy/core 3.11.3
+ @uppy/dashboard 3.8.3
+ @uppy/drag-drop 3.1.0
+ @uppy/file-input 3.1.2
+ @uppy/image-editor 2.4.6
+ @uppy/locales 3.5.3
+ @uppy/progress-bar 3.1.1
+ @uppy/status-bar 3.3.3
+ @uppy/vue 1.1.2
+ @uppy/xhr-upload 3.6.0
+ @vueuse/components 10.9.0
+ @vueuse/core 10.9.0
+ @vueuse/integrations 10.9.0
+ @vueuse/router 10.9.0
+ @vueuse/shared 10.9.0
+ axios 1.7.2
+ codemirror 6.0.1
+ colorjs.io 0.4.3
+ cropperjs 1.5.13
+ dayjs 1.11.7
+ emoji-mart 5.6.0
+ floating-vue 5.2.2
+ fuse.js 6.6.2
+ jsencrypt 3.3.2
+ lodash-es 4.17.21
+ overlayscrollbars 2.5.0
+ overlayscrollbars-vue 0.5.7
+ path-browserify 1.0.1
+ pinia 2.1.6
+ pretty-bytes 6.0.0
+ qrcode 1.5.3
+ qs 6.11.1
+ short-unique-id 5.0.2
+ transliteration 2.3.5
+ ua-parser-js 1.0.38
+ vue 3.4.27
+ vue-demi 0.14.7
+ vue-draggable-plus 0.4.1
+ vue-grid-layout 3.0.0-beta1
+ vue-i18n 9.13.1
+ vue-router 4.3.2

devDependencies:
+ @changesets/cli 2.25.2
+ @iconify/json 2.2.147
+ @intlify/unplugin-vue-i18n 4.0.0
+ @rushstack/eslint-patch 1.3.2
+ @tailwindcss/aspect-ratio 0.4.2
+ @tailwindcss/container-queries 0.1.0
+ @tailwindcss/forms 0.5.7
+ @tsconfig/node18 2.0.1
+ @types/jsdom 20.0.1
+ @types/lodash-es 4.17.12
+ @types/node 18.13.0
+ @types/qs 6.9.7
+ @types/randomstring 1.1.8
+ @types/ua-parser-js 0.7.39
+ @vitejs/plugin-vue 5.0.4
+ @vitejs/plugin-vue-jsx 3.1.0
+ @vitest/ui 0.34.1
+ @vue/compiler-sfc 3.4.27
+ @vue/eslint-config-prettier 7.1.0
+ @vue/eslint-config-typescript 11.0.3
+ @vue/test-utils 2.4.6
+ @vue/tsconfig 0.5.1
+ autoprefixer 10.4.14
+ c8 7.12.0
+ cypress 10.11.0
+ eslint 8.43.0
+ eslint-plugin-cypress 2.13.3
+ eslint-plugin-vue 9.17.0
+ husky 8.0.3
+ jsdom 20.0.3
+ lint-staged 13.2.2
+ npm-run-all 4.1.5
+ postcss 8.4.21
+ postcss-viewport-height-correction 1.1.1
+ prettier 2.8.8
+ prettier-plugin-tailwindcss 0.1.13
+ randomstring 1.2.3
+ rollup-plugin-gzip 3.1.0
+ sass 1.60.0
+ start-server-and-test 1.14.0
+ tailwindcss 3.3.0
+ tailwindcss-safe-area 0.2.2
+ tailwindcss-themer 2.0.3
+ typescript 5.3.3
+ unplugin-icons 0.14.15
+ vite 5.2.11
+ vite-plugin-externals 0.6.2
+ vite-plugin-html 3.2.2
+ vite-plugin-pwa 0.20.0
+ vite-plugin-static-copy 1.0.5
+ vite-plugin-vue-devtools 7.2.1
+ vitest 0.34.1
+ vue-tsc 1.8.27

. prepare$ cd .. && husky install ui/.husky
│ husky - Git hooks installed
└─ Done in 362ms
Done in 3m 41.7s

```

```
  VITE v5.2.11  ready in 949 ms

  ➜  Local:   http://localhost:4000/uc/                                                                                                                                           
  ➜  Local:   http://localhost:3000/console/  
  
  需要替换为代理
  
  http://localhost:8090/console/  
```

![image-20240810192109858](https://biliww.github.io/imgs/md/202408101921076.png)

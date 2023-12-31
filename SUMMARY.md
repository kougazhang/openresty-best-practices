# 目录

* [序](README.md)
* [入门篇](README.md)
    * [Socket 编程发展](base/web_evolution.md)
    * [OpenResty 简介](base/intro.md)
* [Lua 入门](lua/main.md)
    * [Lua 简介](lua/brief.md)
    * [Lua 环境搭建](lua/build_env.md)
    * [Lua 编辑器选择](lua/editor.md)
    * [基础数据类型](lua/class.md)
    * [表达式](lua/operator.md)
    * [控制结构](lua/control_structrues.md)
        * [if/else](lua/if_else.md)
        * [while](lua/while.md)
        * [repeat](lua/repeat.md)
        * [for](lua/for.md)
        * [break，return 和 goto](lua/break.md)
    * [Lua 函数](lua/function_descrip.md)
        * [函数的定义](lua/function_define.md)
        * [函数的参数](lua/function_parameter.md)
        * [函数返回值](lua/function_result.md)
        * [全动态函数调用](lua/call_user_func_array.md)
    * [模块](lua/module.md)
    * [String 库](lua/string_library.md)
    * [Table 库](lua/table_library.md)
    * [日期时间函数](lua/time_date_function.md)
    * [数学库函数](lua/math_library.md)
    * [文件操作](lua/file.md)
* Lua 高阶
    * [元表](lua/metatable.md)
    * [面向对象编程](lua/object_oriented.md)
    * [局部变量](lua/local.md)
    * [判断数组大小](lua/array_size.md)
    * [非空判断](lua/not_nil.md)
    * [正则表达式](lua/re.md)
    * [虚变量](lua/dummy_var.md)
    * [抵制使用 module() 定义模块](lua/not_use_module.md)
    * [调用代码前先定义函数](lua/function_before_use.md)
    * [点号与冒号操作符的区别](lua/dot_diff.md)
    * [module 是邪恶的](lua/module_is_evil.md)
    * [FFI](lua/FFI.md)
    * [什么是 JIT](lua/what_jit.md)
* [Nginx](ngx/nginx.md)
    * [Nginx 新手起步](ngx/nginx_brief.md)
    * [location 匹配规则](ngx/nginx_local_pcre.md)
    * [静态文件服务](ngx/static_file.md)
    * [日志](ngx/nginx_log.md)
    * [反向代理](ngx/reverse_proxy.md)
    * [负载均衡](ngx/balancer.md)
    * [陷阱和常见错误](ngx/pitfalls_and_common_mistakes.md)
* OpenResty
    * [环境搭建](openresty/install.md)
        * [Windows 平台](openresty/install_on_windows.md)
        * [CentOS 平台](openresty/install_on_centos.md)
        * [Ubuntu 平台](openresty/install_on_ubuntu.md)
        * [Mac OS X 平台](openresty/install_osx.md)
    * [Hello World](openresty/helloworld.md)
    * [与其他 location 配合](openresty/work_with_location.md)
    * [获取 uri 参数](openresty/get_url_param.md)
    * [获取请求 body](openresty/get_req_body.md)
    * [输出响应体](openresty/response.md)
    * [日志输出](openresty/log_response.md)
    * [简单 API Server 框架](openresty/simple_api.md)
    * [使用 Nginx 内置绑定变量](openresty/inline_var.md)
    * [子查询](openresty/sub_request.md)
    * [不同阶段共享变量](openresty/share_var.md)
    * [防止 SQL 注入](openresty/safe_sql.md)
    * [如何发起新 HTTP 请求](openresty/how_request_http.md)
    * [如何完成 bit 操作](openresty/bit_brief.md)
        * [一，复习二进制补码](openresty/bit_two's_complement.md)
        * [二，复习位运算](openresty/bit_operations_review.md)
        * [三，LuaJIT 和 Lua BitOp Api](openresty/bit_LuaJIT_BitOp_Api.md)
        * [四，位运算算法实例](openresty/bit_bitwise_operation_example.md)
        * [五，Lua BitOp 的安装](openresty/bit_bitop_installation.md)
* LuaRestyRedisLibrary
    * [访问有授权验证的 Redis](redis/auth_connect.md)
    * [select+set_keepalive 组合操作引起的数据读写错误](redis/select-keeplive.md)
    * [redis 接口的二次封装（简化建连、拆连等细节）](redis/out_package.md)
    * [redis 接口的二次封装（发布订阅）](redis/pub_sub_package.md)
    * [pipeline 压缩请求数量](redis/pipeline.md)
    * [script 压缩复杂请求](redis/script.md)
    * [动态生成的 lua-resty-redis 模块方法](redis/dynamic_redis_module_method.md)
* [LuaCjsonLibrary](json.md)
    * [json 解析的异常捕获](json/parse_exception.md)
    * [稀疏数组](json/sparse_array.md)
    * [空 table 编码为 array 还是 object](json/array_or_object.md)
* [PostgresNginxModule](postgres.md)
    * [调用方式简介](postgres/how_to_use.md)
    * [不支持事务](postgres/not_support_transaction.md)
    * [超时](postgres/timeout.md)
    * [健康监测](postgres/health_check.md)
    * [SQL 注入](postgres/sql_inject.md)
* [LuaNginxModule](ngx_lua.md)
    * [执行阶段概念](ngx_lua/phase.md)
    * [正确的记录日志](ngx_lua/log.md)
    * [热装载代码](ngx_lua/hot_load.md)
    * [阻塞操作](ngx_lua/block_io.md)
    * [缓存](ngx_lua/cache.md)
    * [sleep](ngx_lua/sleep.md)
    * [定时任务](ngx_lua/timer.md)
    * [禁止某些终端访问](ngx_lua/allow_deny.md)
    * [请求返回后继续执行](ngx_lua/continue_after_eof.md)
    * [调试](ngx_lua/debug.md)
    * [请求中断后的处理](ngx_lua/on_abort.md)
    * [我的 lua 代码需要调优么](ngx_lua/lua_opt.md)
    * [变量的共享范围](ngx_lua/lua-variable-scope.md)
    * [动态限速](ngx_lua/lua-limit.md)
    * [shared.dict 非队列性质](ngx_lua/shared_get_keys.md)
    * [正确使用长链接](ngx_lua/keepalive.md)
    * [如何引用第三方 resty 库](ngx_lua/how_use_third_lib.md)
    * [典型应用场景](ngx_lua/use_case.md)
    * [怎样理解 cosocket](ngx_lua/whats_cosocket.md)
    * [如何安全启动唯一实例的 timer ](ngx_lua/how_one_instance_time.md)
    * [如何正确的解析域名](ngx_lua/resolve_the_domain_name.md)
* [LuaRestyDNSLibrary](dns/main.md)
    * [使用动态 DNS 来完成 HTTP 请求](dns/use_dynamic_dns.md)
* [LuaRestyLock](lock.md)
    * [缓存失效风暴](lock/cache-miss-storm.md)
* OpenResty 与 SSL
    * [HTTPS 时代](ssl/introduction.md)
    * [动态加载证书和 OCSP stapling](ssl/certificate.md)
    * [TLS session resumption](ssl/session_resumption.md)
* [测试](test.md)
    * [代码静态分析](test/static_analysis.md)
    * [单元测试](test/unittest.md)
    * [代码覆盖率](test/coverage.md)
    * [API 测试](test/apitest.md)
    * [性能测试](test/performance_test.md)
    * [持续集成](test/ci.md)
    * [灰度发布](test/abtest.md)
      * [分流引擎设计](test/abtest/1.md)
      * [控制台开发](test/abtest/2.md)
      * [向运维平台发展](test/abtest/3.md)
* [Web 服务](web.md)
    * [API 的设计](web/api.md)
    * [数据合法性检测](web/check_data_valid.md)
    * [协议无痛升级](web/switch_protocol.md)
    * [代码规范](web/code_style.md)
    * [连接池](web/conn_pool.md)
    * [C10K 编程](web/c10k.md)
    * [TIME_WAIT 问题](web/time_wait.md)
    * [与 Docker 使用的网络瓶颈](web/docker.md)
* [火焰图](flame_graph.md)
    * [什么是火焰图](flame_graph/what.md)
    * [什么时候使用](flame_graph/when.md)
    * [如何安装火焰图生成工具](flame_graph/install.md)
    * [如何定位问题](flame_graph/how.md)
    * [拓展阅读](flame_graph/other.md)
    * [FAQ](flame_graph/faq.md)

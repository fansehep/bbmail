### BBmail

- bbmail 是一个博客论坛 web 项目, 前端使用 `vue` 开发, 后端使用 `golang` + `gin` + `MySQL` + `Redis`.

#### 技能清单
- 使用 `gin JWT` 来进行认证
- 使用 [`Air`](https://github.com/cosmtrek/air) 进行app 实时重载
- 使用 [`Swagger`](https://github.com/swagger-api) 生成文档
- 使用令牌桶进行全局限流
- 使用 [`go-sqlx`](https://github.com/jmoiron/sqlx) 操作 MySQL, 使用 [`go-redis`](https://github.com/redis/go-redis) 操作 Redis
- 支持 Docker 部署

#### 项目后端目录说明
```Rust
.
├── Dockerfile
├── Makefile
├── README.md
├── conf // app 配置
│   └── config.yaml
├── controller // controller 层
│   ├── code.go
│   ├── comment.go
│   ├── community.go
│   ├── doc_response_models.go
│   ├── post.go
│   ├── post_test.go
│   ├── request.go
│   ├── response.go
│   ├── user.go
│   ├── validator.go
│   └── vote.go
├── dao  // dao 层封装了数据持久层, 操作 mysql, redis
│   ├── mysql
│   │   ├── comment.go
│   │   ├── community.go
│   │   ├── error_code.go
│   │   ├── mysql.go
│   │   ├── post.go
│   │   ├── post_test.go
│   │   └── user.go
│   └── redis
│       ├── error.go
│       ├── keys.go
│       ├── post.go
│       ├── redis.conf
│       ├── redis.go
│       └── vote.go
├── docker-compose.yml
├── docs
│   ├── docs.go
│   ├── swagger.json
│   └── swagger.yaml
├── go.mod
├── go.sum
├── init.sql
├── log
│   └── bluebell-plus.log
├── logger
│   └── logger.go
├── logic
│   ├── community.go
│   ├── post.go
│   ├── truncate.go
│   ├── user.go
│   └── vote.go
├── main.go
├── middlewares
│   ├── auth.go
│   └── ratelimit.go
├── models // 与 mysql 中建表模型相对应
│   ├── comment.go
│   ├── community.go
│   ├── create_tables.sql
│   ├── params.go
│   ├── post.go
│   └── user.go
├── pkg
│   ├── jwt
│   │   └── jwt.go
│   └── snowflake
│       └── gen_id.go
├── routers
│   └── routers.go
├── settings
│   └── settings.go
├── static
│   ├── css
│   │   ├── app.5c39da08.css
│   │   └── chunk-vendors.5b539fe5.css
│   ├── favicon.ico
│   ├── fonts
│   │   ├── element-icons.535877f5.woff
│   │   ├── element-icons.732389de.ttf
│   │   ├── fontello.068ca2b3.ttf
│   │   ├── fontello.8d4a4e6f.woff2
│   │   ├── fontello.a782baa8.woff
│   │   └── fontello.e73a0647.eot
│   ├── img
│   │   ├── avatar.7b0a9835.png
│   │   ├── fontello.9354499c.svg
│   │   ├── iconfont.cdbe38a0.svg
│   │   ├── logo.938d1d61.png
│   │   └── search.8e85063d.png
│   └── js
│       ├── app.81e7c3d0.js
│       ├── app.81e7c3d0.js.map
│       ├── chunk-vendors.218b058e.js
│       └── chunk-vendors.218b058e.js.map
├── templates
│   └── index.html
├── version.go
└── wait-for.sh
```

### 项目预览图

![](/png/2023-10-20_21-10-1697808807.jpg)
# 多语言网站部署说明

## 目录结构
```
Alpha_Optimal_Blog/
├── mkdocs.yml        # 中文配置文件
├── mkdocs.en.yml     # 英文配置文件
├── docs/
│   ├── zh/           # 中文文档
│   └── en/           # 英文文档
└── site/             # 构建输出
    ├── zh/           # 中文站点
    └── en/           # 英文站点
```

## 开发模式

### 启动中文版开发服务器
```bash
mkdocs serve -f mkdocs.yml
```
访问: http://127.0.0.1:8000/

### 启动英文版开发服务器
```bash
mkdocs serve -f mkdocs.en.yml
```
访问: http://127.0.0.1:8000/

## 构建部署

### 构建两个语言版本
```bash
# 构建中文版
mkdocs build -f mkdocs.yml

# 构建英文版
mkdocs build -f mkdocs.en.yml
```

### 部署到服务器
将 `site/` 目录下的内容部署到 web 服务器：
- `site/zh/` → 部署到 `www.alpha-optimal.com/zh/`
- `site/en/` → 部署到 `www.alpha-optimal.com/en/`

## 语言切换功能

网站右上角会显示语言选择器，用户可以在中英文之间切换：
- 在中文页面点击 "English" → 跳转到英文版对应页面
- 在英文页面点击 "中文" → 跳转到中文版对应页面

## 注意事项

1. 中英文文档要保持目录结构一致，以便语言切换时跳转到对应页面
2. 图片等资源文件在两个语言目录中都要存在
3. 每次更新后需要重新构建两个版本

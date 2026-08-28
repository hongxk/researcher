# 科研工作者主页

一个可以直接上传到 GitHub Pages 的静态个人主页，包含四个栏目：首页、生信工具、科研项目、学术论文。

## 文件位置

- `index.html`：网页全部内容
- `README.md`：使用说明

## 本地预览

在 `researcher-homepage` 目录下运行：

```bash
python -m http.server 8000
```

然后浏览器打开 `http://localhost:8000`。

## 发布到 GitHub Pages

1. 登录 GitHub，新建仓库，例如 `researcher-homepage`，选择 Public。
2. 在仓库页面点击 `uploading an existing file`，上传 `index.html` 和 `README.md`。
3. 进入 `Settings` → `Pages`。
4. `Source` 选择 `Deploy from a branch`，分支选 `main`，目录选 `/ (root)`，保存。
5. 等待 1-2 分钟，访问：

```text
https://你的用户名.github.io/researcher-homepage/
```

## 修改个人信息

- 首页：姓名、单位、头像、简介、教育经历、联系链接。
- 生信工具：`tool-card` 卡片，可修改工具名称、描述、技术标签和链接。
- 科研项目：5 个项目已填写，可在 `project-card` 中补充项目描述。
- 学术论文：25 篇论文已填写，可使用搜索、年份、影响因子、引用量筛选。

## 影响因子与引用量

- 影响因子以每条论文的 `data-if` 值为准，请按你的数据维护，OpenAlex 不会覆盖。
- 引用量由 OpenAlex 自动获取，打开页面或点击“刷新数据”即可更新。
- 每篇论文填好 `data-doi` 后才会自动获取引用量。
- 数据会在浏览器中缓存 24 小时。

## 添加论文

复制一条 `<li class="paper">`，填写标题、作者、期刊、年份、`data-if` 和 `data-doi` 即可。

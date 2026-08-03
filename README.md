# leeko-

用于 Loon 与 Surge 的个人图标库和 Loon 规则集。图标、规则文件均可通过公开直链远程引用。

## 图标

图标位于 [`icons/`](./icons)，按用途分类：

```text
icons/
├── app/       # App / 服务图标
├── policy/    # 策略组图标
├── country/   # 国家或地区图标
└── category/  # 分类图标
```

### 复制图标链接

将下面链接中的文件名替换为需要的图标即可。推荐优先使用 jsDelivr；若网络环境不适用，也可使用 GitHub Raw。

| 来源 | 链接模板 |
| --- | --- |
| jsDelivr CDN（推荐） | `https://cdn.jsdelivr.net/gh/leekowen/leeko-@main/icons/app/<文件名>.png` |
| GitHub Raw | `https://raw.githubusercontent.com/leekowen/leeko-/main/icons/app/<文件名>.png` |

示例：

```text
https://cdn.jsdelivr.net/gh/leekowen/leeko-@main/icons/app/stitch.png
```

图标集 JSON：

```text
https://raw.githubusercontent.com/leekowen/leeko-/main/Other/leeko-icons.json
```

可将单个图标链接填入 Loon 的 `img-url` 或 Surge 的 `icon-url`：

```ini
# Loon
Proxy = select, ProxyA, ProxyB, img-url=https://cdn.jsdelivr.net/gh/leekowen/leeko-@main/icons/app/stitch.png

# Surge
Proxy = select, ProxyA, ProxyB, icon-url=https://cdn.jsdelivr.net/gh/leekowen/leeko-@main/icons/app/stitch.png
```

当前已收录：`honor-of-kings.png`、`mobile-legends-bang-bang.png`、`stitch.png`。

## Loon 规则

规则文件位于 [`loon-rules/`](./loon-rules)，可用于补充 Loon 的分流规则。

### 使用方式

1. 打开规则网站，点击规则图标或“导入 Loon”。
2. Loon 打开后确认导入；规则中使用的策略名需已存在于你的配置中。
3. 也可点击“复制规则链接”，再在 Loon 中手动添加远程规则。

当前 `Stitch` 规则仅匹配 `stitch.withgoogle.com`，不预设策略名称；导入后可按自己的配置指定策略。

### 规则网站

<https://leekowen.github.io/leeko-/loon-rules/>

网站支持桌面与移动端：点击图标可直接唤起 Loon，点击按钮可复制规则链接。

### 规则直链

```text
https://raw.githubusercontent.com/leekowen/leeko-/main/loon-rules/stitch.list
```

## 说明

- 图标建议使用正方形 PNG，推荐尺寸 256 × 256 px。
- jsDelivr 存在缓存；更新图标后如未及时生效，可更换文件名或使用版本化路径。
- 请勿在公开规则中提交订阅链接、令牌、账号或其他敏感信息。

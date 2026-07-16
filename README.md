# leeko-

这是一个用于 Loon 与 Surge 配置中远程调用的个人图标库。仓库内的图片可以通过 GitHub Raw 或 jsDelivr CDN 直接引用到策略组、规则集、插件说明或 App 图标配置中。

## 目录结构

```text
icons/
  app/        # App / 服务图标
  policy/     # 策略组图标
  country/    # 国家或地区图标
  category/   # 分类图标
```

## 推荐调用方式

### GitHub Raw URL

```text
https://raw.githubusercontent.com/leekowen/leeko-/main/icons/app/honor-of-kings.png
```

### jsDelivr CDN

```text
https://cdn.jsdelivr.net/gh/leekowen/leeko-@main/icons/app/honor-of-kings.png
```

如果 GitHub Raw 在网络环境里不稳定，优先使用 jsDelivr。

## 已收录图标

```text
icons/app/mobile-legends-bang-bang.png  # 决胜巅峰 / Mobile Legends: Bang Bang
icons/app/honor-of-kings.png            # 王者荣耀国际服 / Honor of Kings
```

## Loon 示例

```ini
[Proxy Group]
Proxy = select, ProxyA, ProxyB, img-url=https://cdn.jsdelivr.net/gh/leekowen/leeko-@main/icons/app/honor-of-kings.png
```

## Surge 示例

```ini
[Proxy Group]
Proxy = select, ProxyA, ProxyB, icon-url=https://cdn.jsdelivr.net/gh/leekowen/leeko-@main/icons/app/mobile-legends-bang-bang.png
```

## 图标上传要求

### 格式

- 首选 PNG。
- 可使用 SVG，但部分客户端或场景兼容性不如 PNG 稳定。
- 不建议使用 JPG，因为透明背景支持不好。

### 尺寸

- 推荐 256 x 256 px。
- 最低建议 128 x 128 px。
- 保持正方形画布，避免长宽不一致。

### 背景

- 推荐透明背景。
- 图标主体居中，四周保留适当留白。
- 深色和浅色界面下都要能看清。

### 文件大小

- 单个图标建议控制在 100 KB 以内。
- 尽量不要上传超大高清图，配置客户端加载时没有必要。

### 文件命名

- 只用小写英文、数字和连字符。
- 不使用中文、空格、特殊符号。
- 示例：

```text
openai.png
youtube.png
proxy.png
direct.png
hong-kong.png
united-states.png
```

### 版权

- 优先使用自己制作、开源授权、或官方允许使用的图标。
- 商标类图标仅建议个人配置使用，不建议打包公开宣传为官方资源。

## 更新图标后的注意事项

- GitHub Raw 通常会较快更新。
- jsDelivr 可能存在缓存。
- 如果 CDN 没有立刻刷新，可以换文件名，或使用带版本的路径。

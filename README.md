# 贪吃蛇 Snake

一个单文件实现的极简贪吃蛇，纯 HTML + Canvas，零依赖。

## 玩法

直接双击 `index.html`，或用任意静态服务器打开：

```bash
python3 -m http.server 8000
# 浏览器访问 http://localhost:8000
```

- 方向键 / `WASD` 控制方向
- `空格` 开始或重新开始
- 手机端在棋盘上滑动
- 每吃一个食物 +10 分，最高分保存在 localStorage
- 撞墙或撞到自己即结束

## 实现

全部逻辑在 `index.html` 内，不依赖任何库或构建步骤。

- 20 × 20 网格，`setInterval` 130ms 驱动一次逻辑帧
- 食物从棋盘上所有空格中随机选取，保证不会生成在蛇身上
- 方向输入做了过滤：不能 180° 掉头，也不能重复设置同方向

## License

MIT

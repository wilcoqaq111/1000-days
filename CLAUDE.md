# 我们的一千天 ❤️

一个记录恋爱1000天点点滴滴的纪念网页。每一天可以展示照片、视频和语音留言，配有背景音乐。

## 项目结构

```
/
├── index.html          # 主页面：展示第N天的照片/视频/语音
├── bgm.mp3             # 背景音乐文件（需自行添加）
├── photos/             # 照片：day1.jpg ~ day1000.jpg
├── videos/             # 视频：day1.mp4 ~ day1000.mp4（可选）
├── voices/             # 语音：day1.mp3 ~ day1000.mp3（可选）
└── .claude/            # Claude Code 配置
```

## 如何运作

- 打开 `index.html` 即可在浏览器中查看
- 页面默认显示第 1 天，通过 **前一天 / 后一天** 按钮切换天数
- 每一天会自动加载对应的媒体文件：
  - 照片：`photos/{日期}-{序号}.jpg` 例如 `photos/2023-10-23-1.jpg`（第1天第1张），支持 jpg/jpeg/png/gif/webp/bmp
  - 视频：`videos/{日期}-{序号}.mp4` 例如 `videos/2023-10-23-1.mp4`
  - 语音：`voices/{日期}.mp3` 例如 `voices/2023-10-23.mp3`
  - 兼容旧格式：`photos/day{天数}.jpg`、`videos/day{天数}.mp4`、`voices/day{天数}.mp3`
- 背景音乐 `bgm.mp3` 循环播放，首次需用户点击页面触发（浏览器自动播放限制）

## 需要准备的文件

1. **背景音乐**：在根目录放入 `bgm.mp3`
2. **照片**：在 `photos/` 文件夹放入 `day1.jpg` ~ `day1000.jpg`，格式为 JPG
3. **视频**（可选）：在 `videos/` 文件夹放入 `day1.mp4` ~ `day1000.mp4`
4. **语音**（可选）：在 `voices/` 文件夹放入 `day1.mp3` ~ `day1000.mp3`

## 自定义配置

在 `index.html` 的 `<script>` 标签顶部可以修改：

- `TOTAL_DAYS`：总天数（默认 1000）
- `currentDay`：起始显示的天数（默认 1）

## 技术栈

纯静态 HTML/CSS/JS，无需服务器，直接用浏览器打开即可。

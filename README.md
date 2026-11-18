# 早报图库（morning-uploader）

[东京大事件](https://github.com/ScareCrowInMountain/market-brief) 频道早报素材的手机上传页，纯静态，托管在 GitHub Pages：
https://scarecrowinmountain.github.io/morning-uploader/

- 首次打开填一个 GitHub 细粒度令牌（仅 `market-brief` 仓库、Contents 读写），存在手机浏览器本地
- Telegram 配置自动从私有仓库 `state/uploader.json` 读取
- 图片：压缩后写入 `assets/morning/`
- 视频：发到 Telegram 取 `file_id`，登记到 `state/video_queue.json`；可选预览版裁剪（1:1/4:5、起点、≤8 秒）与封面（抽帧/选图/首帧）；支持批量
- 队列按时间戳先进先出；点卡片可预览、换封面、删除

单文件 `index.html`，改完 push 到 `main` 约一分钟生效。

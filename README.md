# ExHentai-Lanraragi-Checker

A Tampermonkey userscript that integrates ExHentai/E-Hentai with your Lanraragi library. Automatically checks if galleries are already in your library, marks them with visual indicators, and provides one-click download functionality.

一个 Tampermonkey 用户脚本，用于将 ExHentai/E-Hentai 与您的 Lanraragi 库集成。自动检查图库是否已在您的库中，用视觉标记标识，并提供一键下载功能。

## Features / 功能特性

- ✅ **Auto Library Check** / **自动库检查**: Checks if galleries are already in your Lanraragi library
- 🏷️ **Visual Markers** / **视觉标记**: Marks galleries with different indicators:
  - `(LRR ✔)` - Gallery found in library / 图库已在库中
  - `(LRR！)` - Gallery found via alternative search / 通过备用搜索找到图库
  - `(LRR ❓)` - Check error / 检查错误
- 📥 **Download Integration** / **下载集成**: 
  - Download button on gallery pages / 图库页面上的下载按钮
  - Download links for galleries not in library / 未在库中的图库下载链接
- 🔄 **Progress Monitoring** / **进度监控**: Real-time download status updates
- ⚡ **Concurrent Downloads** / **并发下载**: Supports multiple simultaneous downloads

## Installation / 安装

1. Recommended: Install this script from [GreasyFork](https://greasyfork.org/scripts/558467).  
推荐：从 [GreasyFork](https://greasyfork.org/scripts/558467) 安装此脚本。
2. Alternatively: Manually open the `scrpit.user.js` file, copy all contents, paste them into Tampermonkey, and save the script.  
或：手动打开 `scrpit.user.js` 文件，将全部内容复制粘贴到 Tampermonkey，并保存脚本。


## Configuration / 配置

After installation, edit the user script and modify the following settings:

安装后，编辑用户脚本并修改以下设置：

```javascript
const LRR_SERVER_URL = 'http://127.0.0.1:3000'; // Replace with your Lanraragi server address / 替换为您的 Lanraragi 服务器地址
const LRR_API_KEY = btoa(''); // If your Lanraragi API requires a key, fill it here (automatically converted to base64) / 如果您的 Lanraragi API 需要密钥，请在此填写（自动转为 base64 编码）
```

## Usage / 使用方法

### On Gallery List Pages / 在图库列表页面

- The script automatically checks each gallery and adds visual markers
- Galleries not in your library will show a "下载" (Download) link
- Click the download link to send the gallery to your Lanraragi server

### On Gallery Pages / 在图库页面

- A "下载本页" (Download This Page) button appears in the top-right corner
- Click the button to download the current gallery

### Download Status / 下载状态

- **发送中...** / Sending... - Request is being sent
- **下载中...** / Downloading... - Download is in progress
- **✓ 完成** / ✓ Complete - Download finished successfully
- **✗ 失败/重试** / ✗ Failed/Retry - Download failed (click to retry)


## Credits / 致谢

Forked and modified from [Putarku/LANraragi-scripts](https://github.com/Putarku/LANraragi-scripts)

## Example / 示例

![](image1.png)
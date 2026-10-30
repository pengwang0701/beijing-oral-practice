# 京语练习 · 英语导游口试 PWA

个人备考最小可用版，零依赖静态应用。docs/ 可直接部署到 HTTPS 静态托管。

Safari 打开部署链接 → 分享 → 添加到主屏幕 → 添加。应用和 GitHub Pages 测试站点均无需登录。

开始练习 → 英文系统语音提问（默认隐藏题目）→ 重播或0.75倍慢速 → 录音/手动输入/可选浏览器转写 → 对照双语参考答案 → 勾选自己说到的要点 → 自评掌握或加入错题 → 下一题。

## GitHub Pages

手机测试地址：https://pengwang0701.github.io/beijing-oral-practice/

发布来源：`feat/iphone-pwa` 分支的 `/docs` 文件夹。此分支推送后，GitHub Pages 自动更新。`main` 保留仓库入口，当前 App 尚未合并。

从旧测试域名迁移时，本机进度不会跨域自动转移。请先在旧 App 的“进度”页导出备份，再在新网址导入。Safari 与主屏幕 App 数据也可能分别保存。

## 题库依据

[北京市2026年全国导游资格考试《导游服务能力》参考资料](https://ata-usp.oss-cn-beijing.aliyuncs.com/ueditor%2Fuploadfile%2F20261027%2F090337385163.docx)，由考试平台公开通知附件取得，2026-10-30核对。Word分页依赖排版，不声明与旧对话34页文件逐字相同。

10道题逐项对应原资料知识点；不是官方英文原题，参考答案为简化改写，不是官方标准答案。每题包含原资料章节、原资料链接、答案事实来源。

- 故宫3题：营建年代和时长、明代皇帝数量、博物院成立年份。https://whc.unesco.org/en/list/439/
- 天坛5题：布局、作用、建成年代与原名、主要建筑、祈年殿用途。https://whc.unesco.org/en/list/881/ 及 https://whc.unesco.org/uploads/nominations/881.pdf
- 颐和园1题：仁寿殿用途。https://www.summerpalace.net.cn/displayed.html
- 长城1题：防御体系构成。https://whc.unesco.org/en/list/438/

## 能力与限制

无AI批改、语法纠错、发音评分或自动判对错；反馈根据用户勾选的要点给出练习建议。

真实录音使用MediaRecorder，最长3分钟，仅供本次回听，不上传。离开题目即释放，可先下载。可选浏览器语音识别与录音分开使用，可能经浏览器服务联网处理音频；页面有说明。不支持或失败时可输入，或用iPhone键盘听写。系统英文朗读由SpeechSynthesis提供。

题库进度、错题、自评、文字草稿在本机localStorage保存。可以导出和导入JSON备份；导入前确认替换。Safari与主屏幕App数据可能分开。清除网站数据会删除进度。

首次缓存成功后可离线浏览题库、练习和自评。系统英文朗读离线能力依赖已安装声音；转写可能需要联网。

## 本地启动

在此目录运行 python3 -m http.server 4173 --directory docs ，打开 http://localhost:4173 。iPhone访问需HTTPS部署，普通局域网HTTP不能保证麦克风/PWA功能。

## 验证边界

已检查脚本语法、题库和缓存资源；浏览器走通隐藏题目、输入作答、自查、错题保存。真实iPhone的麦克风、系统语音、语音识别与主屏幕安装尚未真机验证。

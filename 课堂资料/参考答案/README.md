<<<<<<< HEAD
# 第 6 课教师答案

本课是操作验收题。逐项参考结果如下；网址、时间和截图必须来自自己的实际运行，不能照抄教师记录。

|任务|具体操作位置|参考结果|
|---|---|---|
|TODO 01|工程根目录执行 `node tools/check-page.mjs`|检查通过、退出码 0|
|TODO 02|在个人验收副本的 index.html 暂时去掉一个图片 alt 属性|同一检查失败并提示缺失 alt；不要提交为正式作品|
|TODO 03|把该图片的说明性 alt 属性补回原处|再次运行同一检查恢复通过|
|TODO 04|浏览器切换手机尺寸并打开打印预览|无横向溢出、文字可读、作品链接可操作；按手册调整对应 CSS 后重测|
|TODO 05|个人 GitHub 仓库 Settings → Pages，选择 GitHub Actions；使用本工程 .github 中的工作流|对应提交的检查和部署作业通过，访问该次部署给出的 URL|
|TODO 06|只在个人练习分支重复缺少 alt 的故障并推送；观察 Actions 后再修复推送|坏提交检查失败且不发布；修复提交检查通过并发布。当地自检失败不等于已验证远程 Actions|

对照代码在本目录的 `tools/check-page.mjs`、`.github/workflows`、`index.html` 和样式文件中。不要复制别人的 Actions 日志当答案。

合格问题记录必须包含：重现步骤、实际现象、涉及文件、修复内容、同一步骤重测结果。

最终检查：资料、图片、链接、手机布局、导航状态、作品数组、Git 提交和 Pages 网址均正常。提交说明应写清修复原因与结果。
=======
# 第03课：六个任务参考答案

任务文件是 `lesson-03-task.css`。任务编号与操作手册、起步代码统一为 TODO 01—06；不再使用旧的A1/B1编号。

|任务|定位|替换或补充|预期效果|
|---|---|---|---|
|01|.portfolio-list 的 display|block → grid|启用网格|
|02|同一规则的 grid-template-columns|1fr → repeat(2, minmax(0, 1fr))|桌面两列|
|03|.work-cover img 的 object-fit|fill → cover|保持图片比例、裁切超出部分|
|04|.work-card 及 hover/focus-within|下面两条声明|平滑上移，键盘同样有反馈|
|05|max-width:640px媒体查询内部|列数改为1fr|手机一列|
|06|h1 的 font-size|clamp(28px, 6vw, 46px)|标题字号在28—46px之间随视口变化|

任务04分两个位置，不能都写进同一个规则：
```css
.work-card {
  transition: transform 180ms ease, box-shadow 180ms ease;
}
.work-card:hover,
.work-card:focus-within {
  transform: translateY(-4px);
}
```

任务05必须位于媒体查询内部：
```css
@media (max-width: 640px) {
  .portfolio-list { grid-template-columns: 1fr; }
}
```

完整答案见本目录同名CSS。逐项修改自己的任务文件；不要覆盖个人工程。基础验收时不要添加is-auto-grid类，否则可选自适应列数会覆盖两列/一列实验。
>>>>>>> fd2ff791c4748c9abed3b8e099ed764b5f709050

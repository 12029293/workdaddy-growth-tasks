# WorkDaddy 自动化任务：成长任务助手

仓库标记：`WorkDaddyAutomationRepositoryV1`

参考 [workbuddy2api-panel](https://github.com/linguo2625469/workbuddy2api-panel) 的"做任务"能力，用 WorkDaddy 声明式任务实现的成长计划自动化（纯 API，不保存任何 Token/Cookie/密码）。

- [新账号成长任务自动检查](tasks/growth-task-auto-check.json)：账号添加/切换后自动检查一次成长任务，统计未完成数量并弹窗提示，是否执行由用户手动决定。
- [成长任务一键执行](tasks/growth-task-manual-run.json)：手动触发，遍历全部账号，为未完成任务自动报名（accept）、为已完成任务自动领取奖励（claim，web 域），幂等可重复运行。

两个任务配合使用：先由"自动检查"发现未完成任务，再手动运行"一键执行"处理。

创建自己的任务仓库时，把任务 JSON 放进 `tasks/` 目录，并把上面的仓库标记填入仓库简介。

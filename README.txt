打地鼠任务系统 V6（基于测试通过的 V5 重构）

上传结构必须保持：
/index.html
/js/supabase-config.js
/js/task-system.js

不要只上传 index.html，否则任务系统无法加载。

本版新增：
1. 教师可选截止日期；截止时间按所选日期当地时间 23:59:59 记录。
2. 学生打开已关闭或已过期任务时不能进入游戏。
3. 游戏结束提交前再次检查任务状态。
4. 多次尝试继续保留最高分，并记录 attempts。
5. duration_seconds 继续使用“游戏配置时长－剩余时间”。
6. Supabase 与通用任务逻辑移入本地 js 文件，不依赖外部 CDN。

上线前必须先在 Supabase SQL Editor 运行：
supabase_task_status_deadline_migration_v1.sql

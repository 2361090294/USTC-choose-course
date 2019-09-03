# USTC Choose Course

中科大（新）教务系统刷课 Python 小脚本。

> 注意：为了防止脚本的大规模传播，部分代码（两个 TODO 部分共约 7 行代码）已被删去，请通读本脚本并使用浏览器开发者工具弄清楚选课流程后自行补全。
>
> 本脚本是本人学习爬虫等技术的练习作品，仍有不足，开源此脚本的目的也是为了学习交流，欢迎提意见。请勿将选课周期设置过短，以免增大教务网站压力。

## 简介

刷课小脚本，支持直选课和换班。选课成功后会有邮件通知，若出现意外情况也会有邮件通知（可自定义意外后重试的次数）。

直选课时，只传入新课课堂号；换班时，需再传入旧课课堂号和换班理由。

可指定刷课周期和是否采用稳定模式，详见`python main.py -h`。

> 稳定模式中每次选课都重新登录，可用于长时间抢课（如夜间刷漏），短时间抢课不需加入此参数（因为此模式会降低性能）。

## 运行

1. 修改`config.py`的内容，如不需要发邮件，可忽略邮件相关设置；
2. 补全`main.py`中缺失的两个 TODO 部分；
4. 自行使用 pip 工具安装缺失的包；
5. 直选课：`python main.py [new course code]`；
   换班：`python main.py [new course code] [old course code] [reason]`。

详见`python main.py -h`。
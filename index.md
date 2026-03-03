---
title: 京都大阪赏樱出行手册
---

# 京都大阪赏樱出行手册

> 日期：**2026-03-25 - 2026-04-04**  
> 版本：网站 Markdown 版  
> 功能：可快速导航到每一天；进入首页时会根据**浏览器当地时间**，自动跳转到对应日期的行程页。

<div id="auto-jump-status" style="padding:12px 14px;border:1px solid #e5e7eb;border-radius:10px;margin:16px 0;background:#fafafa;">
  正在识别今天日期并尝试跳转...
</div>

## 快速导航

- [Day 1｜3/25（周三）抵达京都 - 轻量版](./days/day-01-2026-03-25.md)
- [Day 2｜3/26（周四）市中心赏樱 + 购物文具线](./days/day-02-2026-03-26.md)
- [Day 3｜3/27（周五）祇园 / 东山固定预约日](./days/day-03-2026-03-27.md)
- [Day 4｜3/28（周六）岚山整天 + 嵯峨野小火车](./days/day-04-2026-03-28.md)
- [Day 5｜3/29（周日）北山 / 下鸭线 + 两顿已订](./days/day-05-2026-03-29.md)
- [Day 6｜3/30（周一）宇治 + 奈良](./days/day-06-2026-03-30.md)
- [Day 7｜3/31（周二）哲学之道 / 南禅寺 / 蹴上 / 冈崎](./days/day-07-2026-03-31.md)
- [Day 8｜4/1（周三）换酒店后走南线：醍醐寺 + 山科](./days/day-08-2026-04-01.md)
- [Day 9｜4/2（周四）轻量补漏日：伏见十石舟 + 京都站](./days/day-09-2026-04-02.md)
- [Day 10｜4/3（周五）京都 → 大阪](./days/day-10-2026-04-03.md)
- [Day 11｜4/4（周六）大阪赏樱收官 + 晚班机](./days/day-11-2026-04-04.md)

## 已订项目总表

- **3/27 午餐**：Gion Matayoshi
- **3/27 晚餐**：YAKINIKU KINOE（19:30，京都时间）
- **3/28 小火车去程**：嵯峨野4号  
  - 10:30 小火车龟冈 -> 10:50 小火车岚山  
  - 座位：2号车厢 12A / 12D
- **3/28 小火车回程**：嵯峨野91号  
  - 18:29 小火车岚山 -> 18:54 小火车龟冈  
  - 座位：富贵5号车厢 4A / 4D
- **3/29 午餐**：Sushi Kawano（13:00，京都时间）
- **3/29 晚餐**：蕎麦酒房 櫟（19:00，预约 ID：25e41c45）
- **二条城 2026 SAKURA NIGHTS 门票**  
  - 订单编号：26KK247540524  
  - 方案名称：【早鸟优惠】周一至周四

## 票券结论

- **一定准备**：ICOCA
- **建议买 Kyoto Subway & Bus 1-Day Pass 的日期**：
  - 3/26
  - 3/27
  - 3/31
  - 4/1
- **建议直接刷 ICOCA 的日期**：
  - 3/28
  - 3/29
  - 3/30
  - 4/2
  - 4/3
  - 4/4（若大阪市区当天地铁搭乘很多次，再考虑 Osaka 1-Day Pass）

## 自动跳转逻辑

首页会按照浏览器当地日期判断是否跳转：

- 如果今天是 **2026-03-25**，自动跳到 Day 1
- 如果今天是 **2026-03-28**，自动跳到 Day 4
- 如果今天是 **2026-04-02**，自动跳到 Day 9
- 如果超出行程日期范围，则停留在首页

> 如果你的网站框架不允许在 Markdown 里直接执行 `<script>`，可以把下面脚本搬到主题的自定义 JS 文件中。

<script>
(function () {
  const tripStart = new Date("2026-03-25T00:00:00");
  const tripEnd = new Date("2026-04-04T23:59:59");
  const now = new Date();

  const status = document.getElementById("auto-jump-status");
  const dayMap = {
    "2026-03-25": { path: "./days/day-01-2026-03-25.md", title: "Day 1｜3/25（周三）抵达京都 - 轻量版" },
    "2026-03-26": { path: "./days/day-02-2026-03-26.md", title: "Day 2｜3/26（周四）市中心赏樱 + 购物文具线" },
    "2026-03-27": { path: "./days/day-03-2026-03-27.md", title: "Day 3｜3/27（周五）祇园 / 东山固定预约日" },
    "2026-03-28": { path: "./days/day-04-2026-03-28.md", title: "Day 4｜3/28（周六）岚山整天 + 嵯峨野小火车" },
    "2026-03-29": { path: "./days/day-05-2026-03-29.md", title: "Day 5｜3/29（周日）北山 / 下鸭线 + 两顿已订" },
    "2026-03-30": { path: "./days/day-06-2026-03-30.md", title: "Day 6｜3/30（周一）宇治 + 奈良" },
    "2026-03-31": { path: "./days/day-07-2026-03-31.md", title: "Day 7｜3/31（周二）哲学之道 / 南禅寺 / 蹴上 / 冈崎" },
    "2026-04-01": { path: "./days/day-08-2026-04-01.md", title: "Day 8｜4/1（周三）换酒店后走南线：醍醐寺 + 山科" },
    "2026-04-02": { path: "./days/day-09-2026-04-02.md", title: "Day 9｜4/2（周四）轻量补漏日：伏见十石舟 + 京都站" },
    "2026-04-03": { path: "./days/day-10-2026-04-03.md", title: "Day 10｜4/3（周五）京都 → 大阪" },
    "2026-04-04": { path: "./days/day-11-2026-04-04.md", title: "Day 11｜4/4（周六）大阪赏樱收官 + 晚班机" }
  };

  const yyyy = now.getFullYear();
  const mm = String(now.getMonth() + 1).padStart(2, "0");
  const dd = String(now.getDate()).padStart(2, "0");
  const key = `${yyyy}-${mm}-${dd}`;

  if (status) {
    status.innerHTML = `检测到本地日期：<strong>${key}</strong>`;
  }

  if (now >= tripStart && now <= tripEnd && dayMap[key]) {
    if (status) {
      status.innerHTML += `<br>2 秒后自动跳转到：<strong>${dayMap[key].title}</strong>`;
    }
    setTimeout(() => {
      window.location.href = dayMap[key].path;
    }, 2000);
  } else {
    if (status) {
      status.innerHTML += "<br>当前日期不在行程范围内，停留在首页。";
    }
  }
})();
</script>

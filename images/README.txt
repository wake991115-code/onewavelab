ONE WAVE LAB 作品集 — 图片放置说明
=====================================

项目目录：D:\Workbuddy-产出\2026-07-27-10-51-08\
本说明文件：images/README.txt

已建好 9 个作品文件夹，文件夹名 = works.js 里的作品 id（一一对应）：
  images/aurora/    images/lumen/    images/city/     images/bloom/
  images/terra/     images/street/   images/nimbus/   images/pulse/   images/drift/


每个文件夹里放图（文件名随你，但建议按顺序命名方便对照）：
  cover.jpg   → 作品封面【必放】  第二页缩略图 + 详情页大图都用它
  01.jpg / 02.jpg / 03.jpg …  → 详情页"项目图集"，想放几张放几张（任意数量，无上限）
  logo.png    → 首页品牌墙真实 logo【选放，不放则显示客户名字标】

说明：图集里的图没有数量上限，文件名只要和你在 works.js 里写的 gallery 路径一致即可。


------------------------------------------------------------
按页面看「图出现在网站的哪个位置」
------------------------------------------------------------

【第一页 index.html · 品牌 logo 墙】  （纯展示，不可点击跳转）
  对应字段：该作品的  logo  字段
  图放哪：  images/<作品id>/logo.png        例：images/aurora/logo.png
  显示效果：首页墙那一格显示这张 logo 图（黑底上自动反相显示）
  不填时：  显示客户名字标（个人项目显示作品名）

【第二页 home.html · 作品网格】  （点任意一格进入详情）
  对应字段：该作品的  img  字段
  图放哪：  images/<作品id>/cover.jpg      例：images/aurora/cover.jpg
  显示效果：网格中这一格的缩略图
  不填时：  显示灰阶色块

【跳转页 project.html · 作品详情页】
  大图：    同 img 字段 → images/<作品id>/cover.jpg
  项目图集：该作品的  gallery  字段（支持任意数量图片）
            普通图双列排布：["images/<作品id>/01.jpg","images/<作品id>/02.jpg", ...]
            某张想满宽（占整行，适合海报/长图）：用对象 {src:"...",full:true}
            例：["images/aurora/01.jpg",{src:"images/aurora/03.jpg",full:true},"images/aurora/02.jpg"]
  不填时：  显示一张灰阶色块占位


------------------------------------------------------------
填 works.js 示例（以 aurora 作品为例）
------------------------------------------------------------
{ id:"aurora", t:"Aurora 品牌升级", cat:"brand", g:"g1", client:"Aurora Tech",
  img:"images/aurora/cover.jpg",
  logo:"images/aurora/logo.png",
  gallery:["images/aurora/01.jpg","images/aurora/02.jpg",{src:"images/aurora/03.jpg",full:true},"images/aurora/04.jpg"],
  role:"品牌 / VI", year:"2025", desc:"为一家新能源科技公司重塑品牌识别……" }

说明：
  - img / logo / gallery 三个字段都是「可选」的，没图就不填，页面自动显示灰阶色块
  - gallery 想放多少张放多少张；标了 full:true 的那张会占满整行（满宽大图）
  - 想让首页墙显示真实 logo，就填 logo；只想换作品图，只填 img 也够


------------------------------------------------------------
使用步骤（放好图后）
------------------------------------------------------------
1. 把图放进对应的 images/<作品id>/ 文件夹，文件名用 cover / 01 / 02 / logo
2. 在 works.js 对应作品填 img / logo / gallery 的路径（参考上面示例）
3. 刷新网页即生效，无需改动任何 HTML


图片建议：
  - 格式 jpg / png 均可
  - 封面与画廊建议长边 ≥ 1600px，单张 ≤ 3MB
  - 首页 logo 用透明背景 PNG 最佳

整理好图片后，直接把图片文件发我，或把「作品名 → 文件名」清单发我，我来帮你写进 works.js。

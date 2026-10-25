<p>在百度搜索中做技术优化（Technical SEO）需要结合百度爬虫的抓取习惯、国内网络环境与站点合规要求。本文以实战教程形式，围绕技术优化排名给出可落地的步骤与注意点，帮助你提升网站在百度的收录与排名效率。</p>
<p>一、先理解百度爬虫与索引逻辑</p>
<p>- 百度对JS渲染的支持逐步完善，但仍建议以服务端渲染（SSR）或预渲染为主，重要内容应在首次响应中可见，避免依赖纯客户端渲染导致无法抓取。</p>
<p>- 抓取频率与抓取预算受站点权重、服务器响应速度和robots设置影响。稳定的服务器与合理的robots、sitemap设置可以提升抓取量。</p>
<p>二、技术SEO核心清单（落地项）</p>
<p>1. HTTPS 与站点安全</p>
<p>- 全站启用HTTPS，避免混合内容。百度倾向安全站点，HTTPS为基础排名因素之一。</p>
<p>2. ICP备案与服务器选择</p>
<p>- 中国大陆用户以国内服务器+备案（ICP备案）为优选，能显著提升访问速度与稳定性，从而间接影响SEO表现。海外服务器配合CDN也可，但注意延迟与法律合规。</p>
<p>3.robots.txt 与 meta robots</p>
<p>- 在根目录配置robots.txt，允许百度抓取必要资源（CSS/JS/图片），避免误屏蔽。对敏感或不想索引的页面使用noindex或disallow。</p>
<p>4.Sitemap 与抓取提交</p>
<p>- 生成XML sitemap（按优先级、变更频率分组），向百度搜索资源平台提交，及时推送新增页面（使用push或接口）。</p>
<p>5.站点结构与内部链接</p>
<p>- 扁平化结构，核心内容尽量3次点击内可达。使用面包屑、站点地图、内部链接让权重合理分散。</p>
<p>6.页面URL与参数处理</p>
<p>- 保持URL简洁、包含关键词、避免 session 参数。对动态参数使用canonical或在搜索资源平台设置参数处理。</p>
<p>7.Canonical 与重复内容</p>
<p>- 对重复页面正确设置rel=\"canonical\"，并在后台避免模板重复生成大量近似页面（如排序、筛选导致的URL爆炸）。</p>
<p>8.重定向与状态码</p>
<p>- 301用于永久重定向，404/410对已下架页面正确返回，避免以200返回空内容误导爬虫。</p>
<p>9.移动优化</p>
<p>- 移动优先：响应式或独立移动站（注意互联标签），确保移动页面与PC页面信息一致。百度强调移动友好性。</p>
<p>10.页面性能优化</p>
<p>- 减少首屏加载时间：启用Gzip/ Brotli压缩，合并/拆分资源，使用HTTP/2或QUIC，合理使用CDN，图片使用WebP/压缩并启用懒加载（可确保可抓取）。</p>
<p>11.JS内容与抓取策略</p>
<p>- 对依赖JS的页面采用SSR、预渲染或动态渲染（动态渲染将预渲染内容返回给爬虫）；对于懒加载或异步渲染的关键内容提供noscript或服务器端渲染保证可抓取。</p>
<p>12.结构化数据</p>
<p>- 使用schema.org标注（JSON-LD、microdata均可），并参考百度的结构化指南以获取丰富摘要（面包屑、产品、评价等）。</p>
<p>13.日志分析与抓取诊断</p>
<p>- 定期分析服务器日志，监测百度蜘蛛抓取频率、抓取错误、404热点页面，优化抓取策略和高频抓取页面。</p>
<p>14.安全与反作弊</p>
<p>- 防止被挂马、被劫持或被大量垃圾URL刷写。保持站点安全、清理恶意链接，必要时使用百度搜索资源平台反馈异常。</p>
<p>三、实施步骤（从0到1）</p>
<p>1.环境与合规检查：确认域名、备案、证书、服务器配置正确，开启HTTPS，检测DNS解析和证书链。</p>
<p>2.基础文件配置：上传规范robots.txt，生成并提交sitemap.xml，设置站点根目录的404页面与301规则。</p>
<p>3.模板与渲染改造：对重要模板做SSR或预渲染，确保首屏文本可见，减少关键数据依赖客户端渲染。</p>
<p>4.性能优化：开启压缩、缓存、CDN，压缩图片、合并资源并启用HTTP/2，测量并压榨首字节时间（TTFB）与首屏时间。</p>
<p>5.结构化与元信息：完善title、description、h1结构，加入schema标注，避免title重复和描述空缺。</p>
<p>6.抓取监控：在百度搜索资源平台绑定站点，提交sitemap，使用抓取诊断、日志分析，对异常页面逐条排查。</p>
<p>7.持续迭代：根据日志和资源平台反馈优化robots、页面速度、内容可抓取性与索引率。</p>
<p>四、常见问题与解决建议</p>
<p>- 页面没被收录：检查是否被robots屏蔽、是否大量重复内容、是否首屏为空或JS渲染失败；使用资源平台抓取并提交。</p>
<p>- 收录但排名差：优化页面速度、提升外链质量、完善用户体验和内容深度。</p>
<p>- 大量参数页面被抓取：在站点上设置参数处理或用canonical合并，避免抓取预算浪费。</p>
<p>- 移动版本不一致：确保移动与桌面版本信息一致，使用rel=alternate/ canonical正确标注（若使用独立移动站）。</p>
<p>五、监控指标与工具</p>
<p>- 百度搜索资源平台：索引量、抓取异常、移动适配、安全告警。</p>
<p>- 服务器日志：爬虫访问频次、响应码分布、耗时。</p>
<p>- 性能工具：PageSpeed、Lighthouse（结合国内测试环境）、实测首屏时间。</p>
<p>- 链接与结构审计：站内链接深度、孤立页面、重复标题。</p>
<p>技术SEO不是一次性工作，而是平台、代码与内容协同优化的长期工程。围绕可抓取性、性能、站点合规与结构化做基础，不断通过日志和百度搜索资源平台反馈迭代，才能在百度搜索中稳步提升收录与排名。实施过程中，优先保证首屏可抓取与稳定的抓取频率，这两点对百度排名影响最大。</p>
https://github.com/RaikageWeave86/repo-j4320zs9/commit/bc18a9749a89a710145f83e8e77e7110d212d838?/713
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/70a8f35cd90217aa8f14ecca0e87be6f94e35ec9?672=ghX
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/70a8f35cd90217aa8f14ecca0e87be6f94e35ec9?/bid?20261025=68
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/70a8f35cd90217aa8f14ecca0e87be6f94e35ec9?/376
https://github.com/RaikageWeave86/repo-j4320zs9/commit/9bf4e18674708ad44fa18d597a072a52814db6fb?161=rlI
https://github.com/RaikageWeave86/repo-j4320zs9/commit/9bf4e18674708ad44fa18d597a072a52814db6fb?/axc?20261025=68
https://github.com/RaikageWeave86/repo-j4320zs9/commit/9bf4e18674708ad44fa18d597a072a52814db6fb?/658
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/ba121f073b766244769cbcd3f71006025098cf69?270=hoU
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/ba121f073b766244769cbcd3f71006025098cf69?/yzu?20261025=46
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/ba121f073b766244769cbcd3f71006025098cf69?/814
https://github.com/RaikageWeave86/repo-j4320zs9/commit/240ef6833aac200c5f097384755cb4c21c603e23?457=ahN
https://github.com/RaikageWeave86/repo-j4320zs9/commit/240ef6833aac200c5f097384755cb4c21c603e23?/krn?20261025=95
https://github.com/RaikageWeave86/repo-j4320zs9/commit/240ef6833aac200c5f097384755cb4c21c603e23?/146
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/6c8e84ffff2a74b130ff654fe0e219b302036eec?680=gnJ
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/6c8e84ffff2a74b130ff654fe0e219b302036eec?/pmq?20261025=16
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/6c8e84ffff2a74b130ff654fe0e219b302036eec?/458
https://github.com/RaikageWeave86/repo-j4320zs9/commit/1ceef8d347eb78b5d1765ac834d2f925c893b35b?949=lcJ
https://github.com/RaikageWeave86/repo-j4320zs9/commit/1ceef8d347eb78b5d1765ac834d2f925c893b35b?/vpn?20261025=04
https://github.com/RaikageWeave86/repo-j4320zs9/commit/1ceef8d347eb78b5d1765ac834d2f925c893b35b?/678
https://github.com/RaikageWeave86/repo-j4320zs9/commit/fefabe90e806c3d8f1ac1b57005da5efd94e0f69?479=cdK
https://github.com/RaikageWeave86/repo-j4320zs9/commit/fefabe90e806c3d8f1ac1b57005da5efd94e0f69?/xag?20261025=36
https://github.com/RaikageWeave86/repo-j4320zs9/commit/fefabe90e806c3d8f1ac1b57005da5efd94e0f69?/027
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/211dfa5ffd916e4bf562c2fd1564ee79401b2786?245=xaB
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/211dfa5ffd916e4bf562c2fd1564ee79401b2786?/xoq?20261025=12
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/211dfa5ffd916e4bf562c2fd1564ee79401b2786?/244
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7788ca6b9ba4f07594193ad0456c85e7c7ee7f68?332=ulH
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7788ca6b9ba4f07594193ad0456c85e7c7ee7f68?/osa?20261025=36
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7788ca6b9ba4f07594193ad0456c85e7c7ee7f68?/449
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b8483a6257876f12d5e00cb5985a2c4e05337b38?168=yvX
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b8483a6257876f12d5e00cb5985a2c4e05337b38?/gxx?20261025=26
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b8483a6257876f12d5e00cb5985a2c4e05337b38?/010
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/086c5f921aea2f4d847e938db6c3acd378f31ebb?579=vcO
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/086c5f921aea2f4d847e938db6c3acd378f31ebb?/vcm?20261025=16
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/086c5f921aea2f4d847e938db6c3acd378f31ebb?/801
https://github.com/RaikageWeave86/repo-j4320zs9/commit/c3ce38418acd56b8aa44733f2e7de140b79b3c69?618=wsJ
https://github.com/RaikageWeave86/repo-j4320zs9/commit/c3ce38418acd56b8aa44733f2e7de140b79b3c69?/qrt?20261025=16
https://github.com/RaikageWeave86/repo-j4320zs9/commit/c3ce38418acd56b8aa44733f2e7de140b79b3c69?/491
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/129143604ff90ad9a1c2b2bebd31c5547bfb9922?019=pmH
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/129143604ff90ad9a1c2b2bebd31c5547bfb9922?/rsj?20261025=96
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/129143604ff90ad9a1c2b2bebd31c5547bfb9922?/342
https://github.com/RaikageWeave86/repo-j4320zs9/commit/5002a201398524592cb9684a73e5757661ecf417?266=cjK
https://github.com/RaikageWeave86/repo-j4320zs9/commit/5002a201398524592cb9684a73e5757661ecf417?/shy?20261025=02
https://github.com/RaikageWeave86/repo-j4320zs9/commit/5002a201398524592cb9684a73e5757661ecf417?/135
https://github.com/RaikageWeave86/repo-j4320zs9/commit/3b06247bc882ab0cc9f4da533edddc62d8657c9b?905=dyI
https://github.com/RaikageWeave86/repo-j4320zs9/commit/3b06247bc882ab0cc9f4da533edddc62d8657c9b?/lvk?20261025=16
https://github.com/RaikageWeave86/repo-j4320zs9/commit/3b06247bc882ab0cc9f4da533edddc62d8657c9b?/023
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/8daf059d5529acad5e97fcc72468636cc9cad745?502=boI
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/8daf059d5529acad5e97fcc72468636cc9cad745?/yso?20261025=38
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/8daf059d5529acad5e97fcc72468636cc9cad745?/714
https://github.com/RaikageWeave86/repo-j4320zs9/commit/006b8d97dfb0d446e721b620cdb04d8dfad72e91?037=zkI
https://github.com/RaikageWeave86/repo-j4320zs9/commit/006b8d97dfb0d446e721b620cdb04d8dfad72e91?/wnv?20261025=99
https://github.com/RaikageWeave86/repo-j4320zs9/commit/006b8d97dfb0d446e721b620cdb04d8dfad72e91?/259
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/f557f46f2148a982e4f808de578ed1f2145e3654?271=pzU
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/f557f46f2148a982e4f808de578ed1f2145e3654?/uei?20261025=19
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/f557f46f2148a982e4f808de578ed1f2145e3654?/829
https://github.com/RaikageWeave86/repo-j4320zs9/commit/ddf063a55e3dba39866a4652ae73753e6f8b781e?703=zpL
https://github.com/RaikageWeave86/repo-j4320zs9/commit/ddf063a55e3dba39866a4652ae73753e6f8b781e?/fkp?20261025=23
https://github.com/RaikageWeave86/repo-j4320zs9/commit/ddf063a55e3dba39866a4652ae73753e6f8b781e?/600
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b8db55a3c7cadeabf42790b0f3dd64536b1dc458?380=vsN
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b8db55a3c7cadeabf42790b0f3dd64536b1dc458?/cti?20261025=92
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b8db55a3c7cadeabf42790b0f3dd64536b1dc458?/056
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/3070870b8398e7309b7a038999915be72ec1f7ce?571=zwK
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/3070870b8398e7309b7a038999915be72ec1f7ce?/mrc?20261025=27
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/3070870b8398e7309b7a038999915be72ec1f7ce?/579
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/33e4c4be2bf66f693ac0587a3b3436410040e80a?572=ntU
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/33e4c4be2bf66f693ac0587a3b3436410040e80a?/sjk?20261025=69
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/33e4c4be2bf66f693ac0587a3b3436410040e80a?/476
https://github.com/RaikageWeave86/repo-j4320zs9/commit/877393137f6afe943186638d6067826e4e4f8a27?692=fkN
https://github.com/RaikageWeave86/repo-j4320zs9/commit/877393137f6afe943186638d6067826e4e4f8a27?/pqk?20261025=72
https://github.com/RaikageWeave86/repo-j4320zs9/commit/877393137f6afe943186638d6067826e4e4f8a27?/699
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7be7238df66d638130b6713fadfa814ec7aa6682?492=fyQ
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7be7238df66d638130b6713fadfa814ec7aa6682?/gur?20261025=84
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7be7238df66d638130b6713fadfa814ec7aa6682?/358
https://github.com/RaikageWeave86/repo-j4320zs9/commit/92b9ca1eac90f0dcbf5ffee1ee62438510b54e4d?837=zwM
https://github.com/RaikageWeave86/repo-j4320zs9/commit/92b9ca1eac90f0dcbf5ffee1ee62438510b54e4d?/rrm?20261025=94
https://github.com/RaikageWeave86/repo-j4320zs9/commit/92b9ca1eac90f0dcbf5ffee1ee62438510b54e4d?/568
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2fb256bcbb91da168941910596234d751eca358d?825=tqR
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2fb256bcbb91da168941910596234d751eca358d?/cgv?20261025=68
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2fb256bcbb91da168941910596234d751eca358d?/924
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b0bdf537d6d25d3753d385a758c9383e7cc20e92?058=tdB
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b0bdf537d6d25d3753d385a758c9383e7cc20e92?/yce?20261025=49
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b0bdf537d6d25d3753d385a758c9383e7cc20e92?/602
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/c8e892088269bbe8da1ea1d87d8462988774f42e?664=rhV
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/c8e892088269bbe8da1ea1d87d8462988774f42e?/nnr?20261025=26
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/c8e892088269bbe8da1ea1d87d8462988774f42e?/625
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0cd99a592e4ddd6385ab1841c2a951ff165f0084?824=lvV
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0cd99a592e4ddd6385ab1841c2a951ff165f0084?/auf?20261025=25
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0cd99a592e4ddd6385ab1841c2a951ff165f0084?/069
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/389927cc196ea068830753789f53202c28f92662?031=ryL
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/389927cc196ea068830753789f53202c28f92662?/efj?20261025=72
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/389927cc196ea068830753789f53202c28f92662?/580
https://github.com/RaikageWeave86/repo-j4320zs9/commit/7b9e81a2e9af307b23cca20ac9c4b579358d545d?058=lfK
https://github.com/RaikageWeave86/repo-j4320zs9/commit/7b9e81a2e9af307b23cca20ac9c4b579358d545d?/jje?20261025=35
https://github.com/RaikageWeave86/repo-j4320zs9/commit/7b9e81a2e9af307b23cca20ac9c4b579358d545d?/202
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/8d9595ed2fedd749c447e52db3fa25476703f349?442=iiY
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/8d9595ed2fedd749c447e52db3fa25476703f349?/cmh?20261025=35
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/8d9595ed2fedd749c447e52db3fa25476703f349?/659
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b9eef7696c0e9856d5f4bb672f05f4c2c29d70ea?102=awP
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b9eef7696c0e9856d5f4bb672f05f4c2c29d70ea?/kyz?20261025=63
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b9eef7696c0e9856d5f4bb672f05f4c2c29d70ea?/060
https://github.com/RaikageWeave86/repo-j4320zs9/commit/9bd2ba3bb5438d93be4d6f639e7fd6ba094e82b3?946=mtQ
https://github.com/RaikageWeave86/repo-j4320zs9/commit/9bd2ba3bb5438d93be4d6f639e7fd6ba094e82b3?/rog?20261025=05
https://github.com/RaikageWeave86/repo-j4320zs9/commit/9bd2ba3bb5438d93be4d6f639e7fd6ba094e82b3?/611
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/54efd3491e86849ad64d79140233ee36dfe835f3?392=vsI
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/54efd3491e86849ad64d79140233ee36dfe835f3?/epl?20261025=35
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/54efd3491e86849ad64d79140233ee36dfe835f3?/591
https://github.com/RaikageWeave86/repo-j4320zs9/commit/605296e63e7e330f79730d81014fb0bf24eb9095?835=krV
https://github.com/RaikageWeave86/repo-j4320zs9/commit/605296e63e7e330f79730d81014fb0bf24eb9095?/hla?20261025=13
https://github.com/RaikageWeave86/repo-j4320zs9/commit/605296e63e7e330f79730d81014fb0bf24eb9095?/010
https://github.com/RaikageWeave86/repo-j4320zs9/commit/f1d14a6bcb8d24c84d6159dd0db25349d4e832f0?467=lbP
https://github.com/RaikageWeave86/repo-j4320zs9/commit/f1d14a6bcb8d24c84d6159dd0db25349d4e832f0?/fmn?20261025=68
https://github.com/RaikageWeave86/repo-j4320zs9/commit/f1d14a6bcb8d24c84d6159dd0db25349d4e832f0?/045
https://github.com/RaikageWeave86/repo-j4320zs9/commit/76ba572d7e92fa3f5a0474311abae27a8a28704c?154=qgL
https://github.com/RaikageWeave86/repo-j4320zs9/commit/76ba572d7e92fa3f5a0474311abae27a8a28704c?/zzv?20261025=18
https://github.com/RaikageWeave86/repo-j4320zs9/commit/76ba572d7e92fa3f5a0474311abae27a8a28704c?/473
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2835147140e982c0d77b14041156befda4146b44?836=otY
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2835147140e982c0d77b14041156befda4146b44?/vph?20261025=58
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2835147140e982c0d77b14041156befda4146b44?/922
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/935f43a803b6f5338515909de6ed8f75359761b5?160=pdA
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/935f43a803b6f5338515909de6ed8f75359761b5?/nac?20261025=33
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/935f43a803b6f5338515909de6ed8f75359761b5?/141
https://github.com/RaikageWeave86/repo-j4320zs9/commit/8c60317c435ce29d2c2d3b1f03a08f14241ac3b9?429=isD
https://github.com/RaikageWeave86/repo-j4320zs9/commit/8c60317c435ce29d2c2d3b1f03a08f14241ac3b9?/aog?20261025=16
https://github.com/RaikageWeave86/repo-j4320zs9/commit/8c60317c435ce29d2c2d3b1f03a08f14241ac3b9?/191
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/b4bf5597ff8385796f36c3f52a85fb538bcb5d1e?270=qrA
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/b4bf5597ff8385796f36c3f52a85fb538bcb5d1e?/oys?20261025=18
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/b4bf5597ff8385796f36c3f52a85fb538bcb5d1e?/148
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0825b8a3a862cdaec5998fc77fb1813104eb3d0d?614=zwB
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0825b8a3a862cdaec5998fc77fb1813104eb3d0d?/dvg?20261025=11
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0825b8a3a862cdaec5998fc77fb1813104eb3d0d?/599
https://github.com/RaikageWeave86/repo-j4320zs9/commit/a75ee427c270558e45318231ac2c8421ba9e7fa4?724=neC
https://github.com/RaikageWeave86/repo-j4320zs9/commit/a75ee427c270558e45318231ac2c8421ba9e7fa4?/izz?20261025=80
https://github.com/RaikageWeave86/repo-j4320zs9/commit/a75ee427c270558e45318231ac2c8421ba9e7fa4?/923
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/c2a69d8b87d0d3593c3398544d3ddb1e5ff95bbb?973=fbY
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/c2a69d8b87d0d3593c3398544d3ddb1e5ff95bbb?/xau?20261025=27
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/c2a69d8b87d0d3593c3398544d3ddb1e5ff95bbb?/657
https://github.com/RaikageWeave86/repo-j4320zs9/commit/7a59de65320a83d026384206e533420f293268bb?582=keP
https://github.com/RaikageWeave86/repo-j4320zs9/commit/7a59de65320a83d026384206e533420f293268bb?/eii?20261025=81
https://github.com/RaikageWeave86/repo-j4320zs9/commit/7a59de65320a83d026384206e533420f293268bb?/886
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/17ef0f7fdedafabb1bcc2b0fe1da17f0d5c768ba?747=pdQ
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/17ef0f7fdedafabb1bcc2b0fe1da17f0d5c768ba?/ths?20261025=37
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/17ef0f7fdedafabb1bcc2b0fe1da17f0d5c768ba?/779
https://github.com/RaikageWeave86/repo-j4320zs9/commit/115dbb689952fdec8cc12e95257337c08998e2d3?351=tqE
https://github.com/RaikageWeave86/repo-j4320zs9/commit/115dbb689952fdec8cc12e95257337c08998e2d3?/bso?20261025=35
https://github.com/RaikageWeave86/repo-j4320zs9/commit/115dbb689952fdec8cc12e95257337c08998e2d3?/471
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2d9b0fb522550fcaea1b274c84b4ba9973bdec14?359=hiC
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2d9b0fb522550fcaea1b274c84b4ba9973bdec14?/ket?20261025=81
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/2d9b0fb522550fcaea1b274c84b4ba9973bdec14?/738
https://github.com/RaikageWeave86/repo-j4320zs9/commit/53d2a378ac347d187200c56583f8acbc8436827f?169=uoW
https://github.com/RaikageWeave86/repo-j4320zs9/commit/53d2a378ac347d187200c56583f8acbc8436827f?/ozi?20261025=36
https://github.com/RaikageWeave86/repo-j4320zs9/commit/53d2a378ac347d187200c56583f8acbc8436827f?/590
https://github.com/RaikageWeave86/repo-j4320zs9/commit/de45169a752f13b78679d3c860f27d2ddcb5d3d6?939=beS
https://github.com/RaikageWeave86/repo-j4320zs9/commit/de45169a752f13b78679d3c860f27d2ddcb5d3d6?/wmj?20261025=31
https://github.com/RaikageWeave86/repo-j4320zs9/commit/de45169a752f13b78679d3c860f27d2ddcb5d3d6?/271
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/afc1ec968765dab1ff65751dd4e485e069317140?692=ttK
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/afc1ec968765dab1ff65751dd4e485e069317140?/sma?20261025=36
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/afc1ec968765dab1ff65751dd4e485e069317140?/356
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0fb55311b225d4546c36d9be2b274b1114dc86af?916=lsB
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0fb55311b225d4546c36d9be2b274b1114dc86af?/iqb?20261025=58
https://github.com/RaikageWeave86/repo-j4320zs9/commit/0fb55311b225d4546c36d9be2b274b1114dc86af?/366
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/807cd4d51215ebf57f29dc16880ddcb91c44177f?281=pfO
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/807cd4d51215ebf57f29dc16880ddcb91c44177f?/tac?20261025=68
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/807cd4d51215ebf57f29dc16880ddcb91c44177f?/358
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b46c9e2871d29d0b0596585abe0589da21bfc801?902=ubX
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b46c9e2871d29d0b0596585abe0589da21bfc801?/thi?20261025=58
https://github.com/RaikageWeave86/repo-j4320zs9/commit/b46c9e2871d29d0b0596585abe0589da21bfc801?/887
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/920ccd7c18a8e166769bef0e1c9766f44f55f0e7?951=usZ
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/920ccd7c18a8e166769bef0e1c9766f44f55f0e7?/zeq?20261025=63
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/920ccd7c18a8e166769bef0e1c9766f44f55f0e7?/864
https://github.com/RaikageWeave86/repo-j4320zs9/commit/91b590dc3b1d883f699c0af85515281b5da18d9d?578=jgY
https://github.com/RaikageWeave86/repo-j4320zs9/commit/91b590dc3b1d883f699c0af85515281b5da18d9d?/wvw?20261025=63
https://github.com/RaikageWeave86/repo-j4320zs9/commit/91b590dc3b1d883f699c0af85515281b5da18d9d?/268
https://github.com/RaikageWeave86/repo-j4320zs9/commit/e73f02c8c8cc574bec48414cbdb2acf5ee4a8837?034=ugJ
https://github.com/RaikageWeave86/repo-j4320zs9/commit/e73f02c8c8cc574bec48414cbdb2acf5ee4a8837?/blc?20261025=58
https://github.com/RaikageWeave86/repo-j4320zs9/commit/e73f02c8c8cc574bec48414cbdb2acf5ee4a8837?/155
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/16206363d306b17fc20010050f6a6f9e8a3a973b?661=mqH
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/16206363d306b17fc20010050f6a6f9e8a3a973b?/wai?20261025=33
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/16206363d306b17fc20010050f6a6f9e8a3a973b?/715
https://github.com/RaikageWeave86/repo-j4320zs9/commit/31e71a1485fe210f70c447073ecb7dec1b84b44c?704=ycW
https://github.com/RaikageWeave86/repo-j4320zs9/commit/31e71a1485fe210f70c447073ecb7dec1b84b44c?/ppr?20261025=82
https://github.com/RaikageWeave86/repo-j4320zs9/commit/31e71a1485fe210f70c447073ecb7dec1b84b44c?/502
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7c351917417177a885297ff2e25bba40eb9337e1?727=lpL
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7c351917417177a885297ff2e25bba40eb9337e1?/ftj?20261025=16
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/7c351917417177a885297ff2e25bba40eb9337e1?/932
https://github.com/RaikageWeave86/repo-j4320zs9/commit/35f5951b7a791dea07c98a563f641867c2a234e2?260=elX
https://github.com/RaikageWeave86/repo-j4320zs9/commit/35f5951b7a791dea07c98a563f641867c2a234e2?/pyj?20261025=27
https://github.com/RaikageWeave86/repo-j4320zs9/commit/35f5951b7a791dea07c98a563f641867c2a234e2?/047
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/de443ef7935248afc2f9f6ccbf12cc51ef3344e4?412=fhJ
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/de443ef7935248afc2f9f6ccbf12cc51ef3344e4?/pnu?20261025=05
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/de443ef7935248afc2f9f6ccbf12cc51ef3344e4?/254
https://github.com/RaikageWeave86/repo-j4320zs9/commit/aaabdb6b88aaf706d9915dc982ca0bb47573ab67?380=ulD
https://github.com/RaikageWeave86/repo-j4320zs9/commit/aaabdb6b88aaf706d9915dc982ca0bb47573ab67?/sds?20261025=56
https://github.com/RaikageWeave86/repo-j4320zs9/commit/aaabdb6b88aaf706d9915dc982ca0bb47573ab67?/365
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/cdb93182fc28783df9a642a6e6ee2193554d8db7?202=akD
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/cdb93182fc28783df9a642a6e6ee2193554d8db7?/ivz?20261025=49
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/cdb93182fc28783df9a642a6e6ee2193554d8db7?/570
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/b0369da305c4569d3a75bcbb8000c24a3c37e609?947=cnT
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/b0369da305c4569d3a75bcbb8000c24a3c37e609?/jkw?20261025=14
https://github.com/selfspawntreasure/repo-a9u3b6yq/commit/b0369da305c4569d3a75bcbb8000c24a3c37e609?/881
https://github.com/RaikageWeave86/repo-j4320zs9/commit/1cf9d5f601d0ec7566febbd0df2f1dc41a1d913a?274=aqV

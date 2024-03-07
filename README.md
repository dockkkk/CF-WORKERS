Cloudflare Worker Vless Sub
这是一个基于 Cloudflare Worker 平台的脚本，在原版的基础上修改了显示 VLESS 配置信息转换为订阅内容。
使用该脚本，你可以方便地将 VLESS 配置信息使用在线配置转换到 Clash 或 Singbox 等工具中。


Telegram交流群：@tweekpiao


在 Cloudflare Worker 控制台中创建一个新的 Worker。
将 worker.js 的内容粘贴到 Worker 编辑器中。
将第 7 行 userID 修改成你自己的 UUID 。
访问订阅内容：

访问 https://[YOUR-WORKERS-URL]/[UUID] 即可获取订阅内容。
例如 https://vless.google.workers.dev/9351bb0c-62ab-40ba-cdc8-27c71d70efa9 就是你的订阅地址。
给 workers绑定 自定义域：

在 workers控制台的 触发器选项卡，下方点击 添加自定义域。
填入你已转入 CloudFlare 域名解析服务的次级域名，例如:vless.google.com后 点击添加自定义域，等待证书生效即可。
如果你是小白，你现在可以直接起飞，不用再往下看了！！！


如果你没有域名，CF的临时域名又容易被墙，那么就继续向下看Pages 高端玩法，绑定免费二级域名，

部署 Cloudflare Pages：

下载 worker.zip 文件，并点上 Star !!!
在 Cloudflare Pages 控制台中选择 上传资产后，为你的项目取名后点击 创建项目，然后上传你下载好的 worker.zip 文件后点击 部署站点。
部署完成后点击 继续处理站点 后，选择 设置 > 环境变量 > 制作为生产环境定义变量 > 添加变量。 变量名称填写UUID，值则为你的UUID，后点击 保存即可。
返回 部署 选项卡，在右下角点击 创建新部署 后，重新上传 worker.zip 文件后点击 保存并部署 即可。
访问订阅内容：

访问 https://[YOUR-PAGES-URL]/[YOUR-UUID] 即可获取订阅内容。
例如 https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10 就是你的订阅地址。
「 我自己有域名！我要绑定自己的域名！我已经熟练的掌握域名解析！ 」
「 我不是小白！我真的真的不是小白！我要玩花活！我要开启高端玩法！ 」
Pages GitHub 部署方法 视频教程
部署 Cloudflare Pages：

在 Github 上先 Fork 本项目，并点上 Star !!!
在 Cloudflare Pages 控制台中选择 连接到 Git后，选中 edgetunnel项目后点击 开始设置。
在 设置构建和部署页面下方，选择 环境变量（高级）后并 添加变量 变量名称填写UUID，值则为你的UUID，后点击 保存并部署即可。
访问订阅内容：

访问 https://[YOUR-PAGES-URL]/[YOUR-UUID] 即可获取订阅内容。
例如 https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10 就是你的订阅地址。
给 Pages绑定 CNAME自定义域：视频教程

在 Pages控制台的 自定义域选项卡，下方点击 设置自定义域。
填入你的自定义次级域名，注意不要使用你的根域名，例如： 您分配到的域名是 fuck.cloudns.biz，则添加自定义域填入 lizi.fuck.cloudns.biz即可；
按照 Cloudflare 的要求将返回你的域名DNS服务商，添加 该自定义域 lizi的 CNAME记录 edgetunnel.pages.dev 后，点击 激活域即可。
如果你是小白，那么你的 pages 绑定自定义域之后即可直接起飞，不用再往下看了！！！
「 我不是小白！我真的真的不是小白！我要玩花活！我要开启高端玩法！ 」
变量说明
变量名	示例	备注	YT
UUID	90cd4a77-141a-43c9-991b-08263cfe9c10	Powershell -NoExit -Command "[guid]::NewGuid()"	Video
PROXYIP	proxyip.fxxk.dedyn.io	备选作为访问CloudFlareCDN站点的代理节点	Video
SOCKS5	user:password@127.0.0.1:1080	优先作为访问CloudFlareCDN站点的SOCKS5代理	Video
SUB	sub.cmliussss.workers.dev	内建域名、IP节点信息的订阅生成器地址	Video
SUBAPI	api.v1.mk	clash、singbox等 订阅转换后端	Video
SUBCONFIG	https://raw.github.../ACL4SSR_Online_Full_MultiMode.ini	clash、singbox等 订阅转换配置文件	Video
RPROXYIP	false	设为 true 即可强制获取订阅器分配的ProxyIP(需订阅器支持)	Video
Star 星星走起
Stargazers over time

已适配自适应订阅内容
v2rayN
clash.meta（Clash Nyanpasu，clash-verge，ClashX Meta）
sing-box（SFI）
感谢
zizifn，3Kmfi6HP，Stanley-baby、ACL4SSR、SHIJS1999，fatkun

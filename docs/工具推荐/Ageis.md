- 应用领域：网络安全
- 分享者：作者菌

众所周知，通过F2A（二次验证）来保证密码安全的应用正在变得越来越流行，不乏网站甚至将其设置为了必须行为，不进行F2A设置便会限制一定功能。

市面上已经存在不少的F2A应用，但它们不是价格高昂（说的就是你，Authy，一个月10 dollar？！你怎么不去抢）、就是国内使用不便（www，Google Authenticator真的很好用）、或者日常抽风（Microsoft你在干什么飞机），因此，我在此推荐免费开源的 *Ageis*

Aegis 可能除了不支持多平台，其他功能都有了。至于云同步，从二次验证的设计初衷来看，似乎也不是必备的。但如果你习惯了使用 1Password、Lastpass 来管理二次验证，那么其实都帮你同步了。

好在 Aegis 支持导入导出，可以非常方便的备份、备份、备份。这是经验之谈啊，丢失二次验证的麻烦程度，远高于丢失密码，动不动就要求你举着证件拍张照，有些甚至不可恢复，总之记得备份…另外记得注意保存应急码。

Aegis 有三种添加二次验证方式，扫码、读取本地二维码图片、手动输入。

如果你已经在其他平台上已经添加了二次验证，那么可以考虑通过手动输入的方式，比如在 1Password 中，二次验证是以 otpauth:// 链接的形式保存的，编辑它，就能看到 secret 信息，将此信息填入 Aegis 中，就完成了二次验证的复制，所以，请保护好你的 secret 信息。

否则迁移二次验证还需要去服务商处开关一次就很麻烦了。

Aegis 的设置页面中，还有其他功能：

 - 深色主题
 - 群组分类
 - 防止截屏
 - 隐藏验证码（点击后显示）
 - 加密数据库（AES-256）
 - 自动锁定应用
 - 导入导出
 - 从其他应用中导入（需要 root）

Aegis 支持从以下应用中导入令牌，但需要 root 权限。包括：

 - Authy
 - FreeOTP
 - FreeOTP+
 - Google Authenticator
 - Steam

 感兴趣的同学可以前往 (GitHub)[https://github.com/beemdevelopment/Aegis] 贡献或研究 Aegis，以及在 (Google Play)[https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis&pli=1] 或 (F-Droid)[https://f-droid.org/en/packages/com.beemdevelopment.aegis] 安装 Aegis。
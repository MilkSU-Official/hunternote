# CVEs

> 范围已收敛到 Android 14+：删除只影响 Android 13/12/更旧版本的条目；索引只按 Android 14、15、16 及厂商/内核研究范围组织。

## 索引

- [按版本查看](indexes/by-version.md) - Android 14/15/16 与厂商/内核研究范围
- [按层级查看](indexes/by-layer.md) - Kernel/Framework/Native/Bootloader/Vendor
- [按组件查看](indexes/by-component.md) - Binder/PMS/GPU/Settings 等
- [按漏洞类型查看](indexes/by-cwe.md) - UAF/OOB/权限提升等

## 漏洞列表

### 2025

| CVE | CVSS | CWE | 层级 | 组件 | 概述 | ITW |
|-----|------|-----|------|------|------|-----|
| [CVE-2025-68260](entries/CVE-2025-68260.md) | N/A | N/A | Kernel | Rust Binder | Linux rust_binder death_list 存在竞态条件；当前不是 Android Security Bulletin 条目。 |  |
| [CVE-2025-48633](entries/CVE-2025-48633.md) | 5.5 | N/A | Framework | DevicePolicyManagerService | DevicePolicyManagerService hasAccountsOnAnyUser 逻辑错误可能在 provisioning 后添加 Device Owner，已被列入 CISA KEV。 | ⭐ |
| [CVE-2025-48593](entries/CVE-2025-48593.md) | 8 | CWE-416 | Native | Bluetooth | Bluetooth bta_hf_client_cb_init UAF 可导致远程代码执行。 |  |
| [CVE-2025-48554](entries/CVE-2025-48554.md) | 6.1 | CWE-693 | Framework | DevicePolicyManagerService | DevicePolicyManagerService handlePackagesChanged 逻辑错误可导致持久拒绝服务。 |  |
| [CVE-2025-48545](entries/CVE-2025-48545.md) | 7.1 | CWE-441 | Framework | AccountManagerService | AccountManagerService isSystemUid confused deputy 可能允许应用访问特权 API。 |  |
| [CVE-2025-48543](entries/CVE-2025-48543.md) | 8.8 | CWE-416 | Native | ART | ART 多处 UAF 可从 Chrome sandbox 攻击 system_server，已被列入 CISA KEV。 | ⭐ |
| [CVE-2025-48535](entries/CVE-2025-48535.md) | 7.8 | CWE-502 | Framework | System/Settings | AppRestrictionsFragment assertSafeToStartCustomActivity unsafe deserialization 可导致 launch-anywhere。 |  |
| [CVE-2025-48530](entries/CVE-2025-48530.md) | 8.1 | CWE-125 | Native | CrabbyAVIF/Media | 多个位置边界检查错误导致越界访问，可能与其他漏洞组合实现远程代码执行。 |  |
| [CVE-2025-48524](entries/CVE-2025-48524.md) | 5.5 | CWE-862 | Framework | WiFi | WifiPermissionsUtil isSystem 缺少权限检查，可能导致本地拒绝服务。 |  |
| [CVE-2025-38352](entries/CVE-2025-38352.md) | 7.4 | CWE-367 | Kernel | Kernel/posix-cpu-timers | Linux posix-cpu-timers 中退出路径与 timer 删除存在竞态，已被列入 CISA KEV。 | ⭐ |
| [CVE-2025-32323](entries/CVE-2025-32323.md) | 7.8 | CWE-20 | Framework | DocumentsUI | DocumentsUI Shared.getCallingAppName 输入校验不当，可通过欺骗性权限弹窗诱导授予文件访问。 |  |
| [CVE-2025-27363](entries/CVE-2025-27363.md) | 8.1 | CWE-787 | Native | FreeType | FreeType 解析 TrueType GX/var 字体 subglyph 结构时存在越界写，已被列入 CISA KEV。 | ⭐ |
| [CVE-2025-26464](entries/CVE-2025-26464.md) | 7.8 | CWE-693 | Framework | AppSearch | AppSearchManagerService executeAppFunction 逻辑错误可导致后台 Activity 启动。 |  |
| [CVE-2025-26443](entries/CVE-2025-26443.md) | 7.3 | CWE-693 | Framework | Text/PackageInstaller | HtmlToSpannedParser parseHtml 逻辑错误可能绕过未知来源安装限制。 |  |
| [CVE-2025-22432](entries/CVE-2025-22432.md) | 6.7 | CWE-20 | Framework | Telecomm | CallRedirectionProcessor notifyTimeout 输入校验不当可能造成持久连接与本地提权。 |  |
| [CVE-2025-22413](entries/CVE-2025-22413.md) | 4 | CWE-703 | Kernel | KVM/pKVM | pKVM hyp-main 多处逻辑错误可能导致本地信息泄露。 |  |
| [CVE-2025-20655](entries/CVE-2025-20655.md) | 5.3 | CWE-125 | Vendor | MediaTek/Keymaster | MediaTek keymaster 缺少边界检查导致越界读，本地攻击者在已取得 System 权限后可能泄露信息。 |  |
| [CVE-2025-0091](entries/CVE-2025-0091.md) | N/A | N/A | Framework | Settings/Account intents | Account 相关 intent 安全检查可因 confused deputy 被绕过，造成本地提权。 |  |
| [CVE-2025-0078](entries/CVE-2025-0078.md) | 8.8 | CWE-250 | Native | Init/SELinux | main.cpp 逻辑错误可能绕过 SELinux，造成本地提权。 |  |
| [CVE-2025-0076](entries/CVE-2025-0076.md) | 3.3 | CWE-862 | Framework | Framework/Core | 多个位置缺少权限检查，可能查看其他用户的图标。 |  |

### 2024

| CVE | CVSS | CWE | 层级 | 组件 | 概述 | ITW |
|-----|------|-----|------|------|------|-----|
| [CVE-2024-53197](entries/CVE-2024-53197.md) | 7.8 | CWE-787 | Kernel | Kernel/ALSA-USB | USB-audio Extigy/Mbox 设备描述符处理可能越界访问，已被列入 CISA KEV。 | ⭐ |
| [CVE-2024-53150](entries/CVE-2024-53150.md) | 7.1 | CWE-125 | Kernel | Kernel/ALSA-USB | USB-audio 查找 clock source 时可能越界读，已被列入 CISA KEV。 | ⭐ |
| [CVE-2024-53104](entries/CVE-2024-53104.md) | 7.8 | CWE-787 | Kernel | Kernel/USB-UVC | UVC frame parsing未跳过 UVC_VS_UNDEFINED 可能导致越界写，已被列入 CISA KEV。 | ⭐ |
| [CVE-2024-50302](entries/CVE-2024-50302.md) | 5.5 | CWE-908 | Kernel | Kernel/HID | Linux HID core report buffer 未清零可能泄露内核内存，已被列入 CISA KEV。 | ⭐ |
| [CVE-2024-49744](entries/CVE-2024-49744.md) | 7.8 | CWE-276 | Framework | AccountManagerService | AccountManagerService parcel mismatch 防护可被 unsafe deserialization 绕过。 |  |
| [CVE-2024-49733](entries/CVE-2024-49733.md) | 5.5 | CWE-200 | Framework | System/Settings | ServiceListing reload 逻辑错误可能允许恶意应用从 Settings 隐藏 NotificationListenerService。 |  |
| [CVE-2024-49721](entries/CVE-2024-49721.md) | N/A | N/A | Framework | InputMethodSubtypeArray | InputMethodSubtypeArray Parcel mismatch 可绕过 key intent 检查并启动任意 Activity。 |  |
| [CVE-2024-45445](entries/CVE-2024-45445.md) | 4 | CWE-459 | Vendor | Huawei/Keystore | Huawei keystore 模块资源未正确关闭或释放，成功利用会影响可用性。 |  |
| [CVE-2024-43093](entries/CVE-2024-43093.md) | 7.3 | CWE-176 | Framework | ExternalStorageProvider | ExternalStorageProvider shouldHideDocument Unicode 规范化处理不当，可绕过敏感目录过滤，已被列入 CISA KEV。 | ⭐ |
| [CVE-2024-43090](entries/CVE-2024-43090.md) | 5 | CWE-862 | Framework | Framework/Core | 多个位置缺少权限检查，可能导致跨用户图片读取。 |  |
| [CVE-2024-43081](entries/CVE-2024-43081.md) | 7.8 | CWE-276 | Framework | PMS | InstallPackageHelper installExistingPackageAsUser 逻辑错误可绕过 carrier restriction。 |  |
| [CVE-2024-43080](entries/CVE-2024-43080.md) | 7.8 | CWE-502 | Framework | System/Settings | AppRestrictionsFragment unsafe deserialization 可导致 launch-anywhere 类本地提权。 |  |
| [CVE-2024-40660](entries/CVE-2024-40660.md) | 7.8 | CWE-276 | Native | SurfaceFlinger | SurfaceFlinger setTransactionState 逻辑错误可能修改受保护显示属性，造成本地提权。 |  |
| [CVE-2024-40652](entries/CVE-2024-40652.md) | 7.3 | CWE-862 | Framework | System/Settings | SettingsHomepageActivity 缺少权限检查，设备配置过程中可能访问 Settings。 |  |
| [CVE-2024-40650](entries/CVE-2024-40650.md) | 7.8 | CWE-358 | Framework | System/Settings | Settings wifi_item_edit_content 缺少 FRP 状态检查，可导致 FRP 绕过。 |  |
| [CVE-2024-36971](entries/CVE-2024-36971.md) | 7.8 | CWE-416 | Kernel | Kernel/Networking | Linux kernel __dst_negative_advice() RCU 规则处理不当导致 UAF，已被列入 CISA KEV。 | ⭐ |
| [CVE-2024-32896](entries/CVE-2024-32896.md) | 8.1 | CWE-783 | Framework | Pixel/Firmware | Pixel 固件/系统逻辑错误可被用于本地提权，已被列入 CISA KEV。 | ⭐ |
| [CVE-2024-29779](entries/CVE-2024-29779.md) | 7.4 | CWE-269 | Native | Keystore/KeyMint | KeyMint legacy 路径存在设备保护绕过/提权风险。 |  |
| [CVE-2024-29745](entries/CVE-2024-29745.md) | 5.5 | CWE-908 | Bootloader | Pixel/Fastboot | Pixel fastboot/firmware 路径存在未初始化数据导致的信息泄露，已被列入 CISA KEV。 | ⭐ |
| [CVE-2024-20865](entries/CVE-2024-20865.md) | 6.6 | CWE-287 | Bootloader | Samsung/Bootloader | Samsung bootloader 认证绕过，物理攻击者可能刷写任意镜像。 |  |
| [CVE-2024-20832](entries/CVE-2024-20832.md) | 6.4 | CWE-20 | Bootloader | Samsung/Bootloader | Samsung Little Kernel bootloader 堆溢出，已获本地特权的攻击者可能执行任意代码。 |  |
| [CVE-2024-0044](entries/CVE-2024-0044.md) | 7.8 | CWE-75 | Framework | PMS | PackageInstallerService createSessionInternal 对 installer package name 处理不当，可导致 run-as 任意应用提权。 |  |
| [CVE-2024-0025](entries/CVE-2024-0025.md) | 7.8 | CWE-284 | Framework | AMS | ActivityManagerService sendIntentSender 逻辑错误可导致后台 Activity 启动，从而造成本地提权。 |  |

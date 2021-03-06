# 期中作業
```
windows sysinternals 技術報告
```

# 下載
```

http://live.sysinternals.com/
http://live.sysinternals.com/procmon.exe
```
# 官方網址
```
https://docs.microsoft.com/en-us/sysinternals/
```
# 經典教材
```
Troubleshooting with the Windows Sysinternals Tools (2ND ed.
英文/Mark E. Russinovich, Aaron Margosis
Microsoft Press出版日期：2016-10-17

Windows Sysinternals 實戰指南
馬克·拉西諾維 (Mark Russinovich), 艾倫·馬格西斯 (Aaron Margosis)
人民郵電出版社出版日期：2017-10-01
```
```
Windows Sysinternals creator Mark Russinovich and Aaron Margosis show you how to:

Use Process Explorer to display detailed process and system information
Use Process Monitor to capture low-level system events, 
and quickly filter the output to narrow down root causes
List, categorize, and manage software that starts 
when you start or sign in to your computer, 
or when you run Microsoft Office or Internet Explorer
Verify digital signatures of files, of running programs, 
and of the modules loaded in those programs
Use Autoruns, Process Explorer, Sigcheck, 
and Process Monitor features that can identify and clean malware infestations
Inspect permissions on files, keys, services, shares, and other objects
Use Sysmon to monitor security-relevant events across your network
Generate memory dumps when a process meets specified criteria
Execute processes remotely, and close files that were opened remotely
Manage Active Directory objects and trace LDAP API calls
Capture detailed data about processors, memory, and clocks

Troubleshoot unbootable devices, file-in-use errors, 
unexplained communication, and many other problems
Understand Windows core concepts that aren’t well-documented elsewhere
```

```
第1部分入門
第1章Sysinternals工具入門3 
第2章Windows核心概念13 
第3章Process Explorer36 
第4章Autoruns95 

第2部分使用指導
第5章Process Monitor125 
第6章Proc Dump165 

第7章Ps Tools187 

第8章進程和診斷工具221 
第9章安全工具259 
第10章ActiveDirectory工具304 
第11章桌面工具320 
第12章文件工具333 
第13章磁盤工具343 
第14章網絡和通信工具360 
第15章系統信息工具371 
第16章其他工具391 

第3部分排錯——“難解之謎” 
第17章錯誤信息397 
第18章崩潰419 
第19章掛起和性能遲鈍429 
第20章惡意軟件455 
第21章理解系統行為502 
第22章開發者排錯521
```
# 第1部分入門
```
第1章Sysinternals工具入門3 
工具概述3 
Windows Sysinternals網站6 
下載工具6 
直接通過網絡運行工具8 
單一可執行映像9 
Windows Sysinternals論壇9 
Windows Sysinternals網站博客10 
Mark的博客10 
Mark的網絡廣播11 
Sysinternals許可信息11 
最終用戶許可協議以及／accepteula參數11 
有關Sysinternals許可的常見問題12 

第2章Windows核心概念13 
管理權利14 
進程、線程和作業16 
用戶模式和內核模式17 
句柄18 
應用程序隔離19 
應用容器20 
受保護進程24 
調用棧和符號26 
調用棧是什麼？26 
符號是什麼？27 
符號的配置29 
會話、窗口站、桌面和窗口消息30 
遠程桌面服務會話31 
窗口站32 
桌面33 
窗口消息34 

第3章Process Explorer36 
Procexp概述36
度量CPU的使用情況38 
管理權利39 
主窗口40 
進程列表40 
定制可顯示的列49 
保存顯示的數據60 
工具欄參考60 
找出窗口對應的進程61 
狀態欄62 
DLL和句柄63 
查找DLL或句柄63 
DLL視圖64 
句柄視圖67 
進程詳情71 
Image選項卡71 
Performance選項卡73 
Performance Graph選項卡74 
GPUGraph選項卡74 
Threads選項卡75 
TCP／IP選項卡75 
Security選項卡76 
Environment選項卡77 
Strings選項卡78 
Services選項卡79 
.NET選項卡79 
Job選項卡80 
線程詳情81 
驗證映像簽名83 
VirusTotal分析84 
系統信息86 
CPU選項卡88 
Memory（內存）選項卡88 
I／O選項卡89 
GPU選項卡89 
顯示選項91 
用Procexp取代任務管理器92 
通過Procexp啟動進程93
其他用戶的會話93 
其他功能93 
關機選項93 
命令行參數94 
恢復Procexp的默認值94 
鍵盤快捷鍵參考94 

第4章Autoruns95 
Autoruns基礎知識96 
禁用或刪除自動啟動項98 
Autoruns和管理權利99 
驗證代碼簽名99 
VirusTotal分析100 
隱藏自動啟動項101 
進一步了解某個自動啟動項103 
查看其他用戶的自動啟動項104 
查看脫機系統的ASEP104 
更改字體105 
不同類型的自動啟動105 
Logon105 
Explorer107 
Internet Explorer109 
Scheduled Tasks109 
Services110 
Drivers110 
Codecs111 
Boot Execute111 
Imagehijacks112 
App Init113 
Known DLLs113 
Winlogon114 
Winsock Providers114 
Printmonitors115 
LSAproviders115
Networkproviders116 
WMI116 
Sidebargadgets116 
Office116 
保存並對比結果117 
保存為製表符分隔的文本117 
保存為二進制（.arn）格式118 
查看並對比保存的結果118 
AutorunsC118 
Autoruns和惡意軟件121 
```
# 第2部分使用指導
```
第5章Process Monitor125 
Procmon概述126 
事件127 
理解默認顯示的列128 
定制要顯示的列130 
事件屬性對話框132 
查看Profiling事件135 
查找事件137 
複製事件數據137 
跳轉至註冊表或文件位置138 
聯機搜索138 
篩選、強調和收藏138 
配置篩選器139 
配置強調141 
收藏141 
高級輸出142 
保存篩選器以待後用143 
進程樹143 
保存並打開Procmon的追踪記錄145 
保存Procmon的追踪記錄145 
Procmon的XML架構147 
打開保存的Procmon追踪記錄149 
記錄啟動、註銷後及關機活動150
記錄啟動過程150 
讓Procmon在賬戶註銷後繼續運行151 
長時間運行追踪以及日誌文件體積的控制152 
丟棄篩選掉的事件152 
歷史深度153 
備份文件153 
配置設置的導入和導出154 
Procmon的自動化操作：命令行選項154 
分析工具156 
Process Activity Summary157 
File Summary157 
Registry Summary159 
Stack Summary160 
Network Summary161 
Cross Reference Summary161 
Count Occurrences161 
將自定義調試輸出注入Procmon追踪162 
工具欄參考163 

第6章Proc Dump165 
命令行語法167 
指定要監視的進程168 
附加至現有進程169 
啟動目標進程170 
監視通用Windows平台應用程序170 
通過Ae Debug註冊自動啟用調試172 
指定轉儲文件路徑173 
指定創建轉儲的條件174 
監視異常178 
轉儲文件選項179 
Miniplus轉儲181
Proc Dump和Procmon：配合使用效果更好183 
以非交互方式運行Proc Dump185 
在調試器中查看轉儲185 

第7章Ps Tools187 
通用功能188 
遠程操作188 
遠程Ps Tools連接排錯190 
Ps Exec191 
遠程進程的退出192 
重定向控制台輸出193 
Ps Exec的備用憑據194 
Ps Exec的命令行選項194 
進程性能選項195 
遠程連接選項196 
運行時環境選項196 
PsFile199 
PsGetSid200 
PsInfo201 
PsKill203 
PsList204 
PsLoggedon205 
PsLogList206 
PsPasswd210 
PsService211 
Query211 
Config213 
Depend214 
Security214 
Find215 
Set Config215 

啟動、停止、重啟動、暫停、恢復215 
PsShutdown215 
PsSuspend218 
PsTools的命令行語法218
PsExec218 
PsFile219 
PsGetSid219 
PsInfo219 
PsKill219 
PsList219 
PsLoggedOn219 
PsLogList219 
PsPasswd219 
PsService219 
PsShutdown220 
PsSuspend220 
PsTools系統要求220 

第8章進程和診斷工具221 
VMMap221 
啟動VMMap並選擇進程222 
VMMap窗口224 
內存類型225 
內存信息226 
時間線和快照227 
查看內存區域中包含的文本229 
查找並複製文本229 
查看已安排進程的分配229 
地址空間碎片232 
保存並加載快照結果233 
VMMap的命令行選項233 
恢復VMMap的默認值234 
DebugView234 
調試輸出是什麼？234 
DebugView顯示的內容235 
捕獲用戶模式的調試輸出237 
捕獲內核模式調試輸出237 
輸出結果的搜索、篩选和強調238 
保存、日誌和打印241 
遠程監視242
LiveKd244 
LiveKd的前提需求245 
運行LiveKd245 
內核調試器的目標類型246 
輸出至調試器或轉儲文件247 
內容轉儲248 
Hyper—V來賓調試249 
符號249 
LiveKd使用範例250 
ListDLLs251 
Handle254 
顯示和搜索句柄255 
句柄數257 
關閉句柄258 

第9章安全工具259 
SigCheck259 
指定要掃描的文件262 
簽名驗證263 
VirusTotal分析265 
有關文件的其他信息267 
輸出格式268 
雜項269 
AccessChk270 
“有效權限”是什麼？271 
AccessChk的使用271 
對像類型273 
搜索訪問權利276 
輸出選項277 
Sysmon279 
Sysmon可記錄的事件280 
Sysmon的安裝和配置287 
提取Sysmon事件數據291 
AccessEnum293 
ShareEnum295 
ShellRunAs296 
Autologon297
LogonSessions298 
SDelete301 
SDelete的使用302 
SDelete的工作原理302 

第10章ActiveDirectory工具304 
AdExplorer304 
連接到域304 
AdExplorer顯示的內容305 
對象306 
特性307 
搜索308 
快照309 
AdExplorer的配置310 
AdInsight310 
AdInsight的數據捕獲311 
顯示選項313 
查找感興趣的信息314 
篩選結果316 
保存和導出AdInsight的數據317 
命令行選項318 
AdRestore319 

第11章桌面工具320 
BgInfo320 
配置要顯示的數據321 
外觀選項324 
保存BgInfo配置以供後用325 
其他輸出選項325 
更新其他桌面327 
Desktops327 
ZoomIt329 
ZoomIt的使用329 
放大模式330 
繪圖模式330 
鍵入模式331 
休息計時器331 
LiveZoom331

第12章文件工具333 
Strings333 
Streams334 
NTFS鏈接工具335 
Junction336 
FindLinks338 
DiskUsage（DU）338 
重啟後文件操作工具341 
PendMoves341 
MoveFile341 

第13章磁盤工具343 
Disk2Vhd343 
Sync349 
DiskView350 
Contig352 
整理現有文件的碎片353 
分析現有文件的碎片化程度354 
分析可用空間的碎片程度355 
創建連續的文件355 
DiskExt356 
LDMDump357 
VolumeID359 

第14章網絡和通信工具360 
PsPing360 
ICMPPing361 
TCPPing362 
PsPing服務器模式363 
TCP／UDP延遲測試364 
TCP／UDP帶寬測試366 
PsPing直方圖367 
TCPView368 
Whois369 

第15章系統信息工具371 
RAMMap371 
UseCounts372
Processes374 
PrioritySummary374 
PhysicalPages375 
PhysicalRanges376 
FileSummary376 
FileDetails377 
清理物理內存378 
保存和加載快照378 
RegistryUsage（RU）379 
CoreInfo381 
—c：有關內核的信息382 
—f：內核功能信息382 
—g：有關處理器組的信息384 
—l：有關緩存的信息384 
—m：NUMA訪問成本385 
—n：有關NUMA節點的信息386 
—s：有關插槽的信息386 
—v：與虛擬化有關的功能386 
WinObj386 
LoadOrder388 
PipeList389 
ClockRes390 

第16章其他工具391 
RegJump391 
Hex2Dec392 
RegDelNull392 
BluescreenScreenSaver393 
Ctrl2Cap394 
```
# 第3部分排錯——“難解之謎”
```
第17章錯誤信息397 
錯誤信息排錯397 
案例：文件夾被鎖定399
案例：文件正在使用中錯誤400 
案例：照片查看器的未知錯誤401 
案例：ActiveX註冊失敗402 
案例：“播放到”失敗404 
案例：安裝失敗404 
排錯405 
具體分析407 
案例：不可讀取的文本文件409 
案例：文件夾關聯丟失410 
案例：臨時註冊表配置文件412 
案例：OfficeRMS錯誤416 
案例：林功能級別提升失敗417 

第18章崩潰419 
崩潰故障的排錯419 
案例：反病毒軟件更新失敗422 
案例： Proksi工具的崩潰423 
案例：網絡位置感知服務的故障424 
案例：EMET升級失敗425 
案例：崩潰轉儲丟失426 
案例：無規律卡頓427 

第19章掛起和性能遲鈍429 
掛起和性能遲鈍問題的排錯429 
案例：IExplore耗盡CPU431 
案例：失控的網站432 
案例：ReadyBoost造成的問題434 
案例：筆記本藍光播放器卡頓436 
案例：公司內網長達15分鐘的登錄438 
案例：PayPal郵件掛起439 
案例：財務軟件掛起441 
案例：緩慢的主題演講演示442 
案例：Project文件打開緩慢4 46
複合案例：Outlook掛起450 

第20章惡意軟件455 
惡意軟件排錯456 
Stuxnet（震網）458 
惡意軟件和Sysinternals工具459 
Stuxnet的傳播介質459 
WindowsXP上的Stuxnet460 
深入調查463 
通過篩選查找相關事件463 
Stuxnet對系統的改動465 
.PNF文件469 
Windows7中的特權提升471 
借助Sysinternals工具發現的Stuxnet473 
案例：奇怪的重啟動474 
案例：假冒的Java更新程序477 
案例：Winwebsec恐嚇軟件480 
案例：失控的GPU487 
案例：莫名其妙的FTP連接488 
案例：服務的錯誤配置491 
案例：阻止Sysinternals的惡意軟件494 
案例：殺進程的惡意軟件496 
案例：假冒系統組件498 
案例：神秘的ASEP499 

第21章理解系統行為502 
案例：Q：盤502 
案例：莫名其妙的網絡連接505 
案例：短命的進程506 
案例：應用安裝記錄器510 
案例：未知的NTLM通信516 

第22章開發者排錯521
案例：被破壞的Kerberos委派521 
案例：ProcDump內存洩漏522
```

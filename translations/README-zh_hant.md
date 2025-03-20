<p>
  <a href="https://blog.bytebytego.com/?utm_source=site"><img src="../images/banner.jpg" /> </a>
</p>

<p align="center">
  【
  <a href="https://www.youtube.com/channel/UCZgt6AzoyjslHTC9dz0UoTw">
    👨🏻‍💻 YouTube
  </a> | 
  <a href="https://blog.bytebytego.com/?utm_source=site">
    📮 Newsletter
  </a> 】
</p>

<a href="https://trendshift.io/repositories/3709" target="_blank"><img src="https://trendshift.io/api/badge/repositories/3709" alt="ByteByteGoHq%2Fsystem-design-101 | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>

# 系統設計 101（System Design 101）

運用視覺化和簡單術語來解釋複雜系統。

無論你是在準備系統設計面試，還是純粹想了解系統的底層運作原理，我們都希望這個Repo可以幫助你達成此目標。

# 目錄

<!-- TOC toc.levels=2 -->

- [系統設計 101（System Design 101）](#系統設計-101system-design-101)
- [目錄](#目錄)
    - [通訊協定](#通訊協定)
        - [REST API vs. GraphQL](#rest-api-vs-graphql)
        - [gRPC 是如何運作的？](#grpc-是如何運作的)
        - [什麼是 webhook？](#什麼是-webhook)
        - [如何提升 API 效能？](#如何提升-api-效能)
        - [HTTP 1.0 -\> HTTP 1.1 -\> HTTP 2.0 -\> HTTP 3.0 (QUIC)](#http-10---http-11---http-20---http-30-quic)
        - [SOAP vs REST vs GraphQL vs RPC](#soap-vs-rest-vs-graphql-vs-rpc)
        - [Code First vs. API First](#code-first-vs-api-first)
        - [HTTP 狀態碼](#http-狀態碼)
        - [API Gateway 有什麼作用？](#api-gateway-有什麼作用)
        - [我們要如何設計高效安全的 API？](#我們要如何設計高效安全的-api)
        - [TCP/IP 封裝](#tcpip-封裝)
        - [為什麼 Nginx 被叫做「反向」代理？](#為什麼-nginx-被叫做反向代理)
        - [常見的負載平衡演算法有哪些？](#常見的負載平衡演算法有哪些)
        - [URL，URI，URN - 你知道它們的區別嗎？](#urluriurn---你知道它們的區別嗎)
    - [CI/CD](#cicd)
        - [簡單解釋 CI/CD Pipeline](#簡單解釋-cicd-pipeline)
        - [Netflix 技術堆疊（CI/CD Pipeline）](#netflix-技術堆疊cicd-pipeline)
    - [架構模式](#架構模式)
        - [MVC、MVP、MVVM、MVVM-C 和 VIPER](#mvcmvpmvvmmvvm-c-和-viper)
        - [每一位開發者都應該知道的 18 種關鍵設計模式](#每一位開發者都應該知道的-18-種關鍵設計模式)
    - [資料庫](#資料庫)
        - [關於雲端服務中不同類型的資料庫的一個方便速查表](#關於雲端服務中不同類型的資料庫的一個方便速查表)
        - [8 種支援資料庫的資料結構](#8-種支援資料庫的資料結構)
        - [一行 SQL 語法在資料庫中是如何執行的？](#一行-sql-語法在資料庫中是如何執行的)
        - [CAP 理論](#cap-理論)
        - [記憶體和儲存的類型](#記憶體和儲存的類型)
        - [視覺化 SQL 查询](#視覺化-sql-查询)
        - [SQL 語言](#sql-語言)
    - [快取](#快取)
        - [快取無所不在](#快取無所不在)
        - [為什麼 Redis 這麼快？](#為什麼-redis-這麼快)
        - [Redis 的使用場景](#redis-的使用場景)
        - [最佳快取策略](#最佳快取策略)
    - [微服務架構](#微服務架構)
        - [典型的微服務架構是什麼樣的？](#典型的微服務架構是什麼樣的)
        - [微服務最佳實踐](#微服務最佳實踐)
        - [微服務通常使用哪些技術堆疊？](#微服務通常使用哪些技術堆疊)
        - [為什麼 Kafka 那麼快？](#為什麼-kafka-那麼快)
    - [支付系統](#支付系統)
        - [如何學習支付系統？](#如何學習支付系統)
        - [為什麼信用卡被稱為「銀行最賺錢的產品」？VISA/萬事達是如何賺錢的？](#為什麼信用卡被稱為銀行最賺錢的產品VISA萬事達是如何賺錢的)
        - [當我們在店家刷卡時，VISA 是如何運作的？](#當我們在店家刷卡時visa-是如何運作的)
        - [世界各地的支付系統系列（第一部分）：印度的統一支付介面（Unified Payments Interface，UPI）](#世界各地的支付系統系列第一部分印度的統一支付介面unified-payments-interfaceupi)
    - [DevOps](#devops)
        - [DevOps vs. SRE vs. 平台工程（Platform Engineering）。有何不同？](#devops-vs-sre-vs-平台工程platform-engineering有何不同)
        - [k8s（Kubernetes）是什么？](#k8skubernetes是什么)
        - [Docker vs. Kubernetes。我们应该用哪一个？](#docker-vs-kubernetes我们应该用哪一个)
        - [Docker 的工作原理](#docker-的工作原理)
    - [GIT](#git)
        - [Git 指令是如何運作的？](#git-指令是如何運作的)
        - [Git 的工作原理](#git-的工作原理)
        - [Git merge vs. Git rebase](#git-merge-vs-git-rebase)
    - [雲端服務](#雲端服務)
        - [不同雲端服務的便捷速查表（2023 年版本）](#不同雲端服務的便捷速查表2023-年版本)
        - [什麼是雲端原生（cloud native）？](#什麼是雲端原生cloud-native)
    - [開發者生產力工具](#開發者生產力工具)
        - [視覺化 JSON 文件](#視覺化-json-文件)
        - [自动将代码转换为架構图](#自动将代码转换为架構图)
    - [Linux](#linux)
        - [Linux 文件系统解析](#linux-文件系统解析)
        - [你应该知道的 18 个最常用的 Linux 指令](#你应该知道的-18-个最常用的-linux-指令)
    - [安全](#安全)
        - [HTTPS 是如何運作的？](#https-是如何運作的)
        - [简明扼要解释下 Oauth 2.0。](#简明扼要解释下-oauth-20)
        - [四种最常见的身份认证机制](#四种最常见的身份认证机制)
        - [会话、Cookie、JWT、令牌、SSO 和 OAuth 2.0 - 它们分别是什么？](#会话cookiejwt令牌sso-和-oauth-20---它们分别是什么)
        - [如何将密码安全地存储到資料庫中，以及如何验证密码？](#如何将密码安全地存储到資料庫中以及如何验证密码)
        - [向一个十岁小孩解释 JSON Web Token (JWT)](#向一个十岁小孩解释-json-web-token-jwt)
        - [Google Authenticator（或者其它类型的两步认证器）是如何運作的？](#google-authenticator或者其它类型的两步认证器是如何運作的)
    - [真实案例学习](#真实案例学习)
        - [Netflix 的技術堆疊](#netflix-的技術堆疊)
        - [Twitter 架構 2022](#twitter-架構-2022)
        - [过去 15 年 Airbnb 微服務架構的演进之路](#过去-15-年-airbnb-微服務架構的演进之路)
        - [Monorepo vs. Microrepo.](#monorepo-vs-microrepo)
        - [如果是你，你要如何设计 Stack Overflow 网站？](#如果是你你要如何设计-stack-overflow-网站)
        - [為什麼 Amazon Prime Video 监控从无服务（Serverless）转向了單體架（Monolithic）？它是怎样节省九成成本的呢？](#為什麼-amazon-prime-video-监控从无服务serverless转向了單體架monolithic它是怎样节省九成成本的呢)
        - [Disney Hotstar 是如何在锦标赛期间捕获 50 亿个表情符号的？](#disney-hotstar-是如何在锦标赛期间捕获-50-亿个表情符号的)
        - [Discord 是怎样存储数万亿条消息的](#discord-是怎样存储数万亿条消息的)
        - [YouTube、TikTok Live 或 Twitch 上的视频直播是如何運作的呢？](#youtubetiktok-live-或-twitch-上的视频直播是如何運作的呢)


<!-- /TOC -->

## 通訊協定

架構風格定義了應用程式介面（application programming interface，API）的不同元件之間是如何相互互動的。因此，透過提供設計和建構 API 的標準方法，它們一起保證了效率、可靠性以及與其他系統整合的便捷性。以下是最常用的風格：

<p>
  <img src="../images/api-architecture-styles.png" style="width: 640px">
</p>

- SOAP：

  成熟、全面、基於 XML

  最適合企業應用

- RESTful：

  流行、易於實現、基於 HTTP 方法

  理想的 Web 服務

- GraphQL：

  查詢語言，請求特定資料

  減少網路負擔，回應速度更快

- gRPC：

  現代、高效能、基於 Protocol Buffers

  適合微服務架構

- WebSocket：

  即時、雙向、持久連線

  非常適合低延遲資料交換

- Webhook：

  事件驅動、HTTP 回調、非同步

  當事件發生時通知系統


### REST API vs. GraphQL

在 API 設計方面，REST 和 GraphQL 各有其優劣。

下圖顯示了 REST 和 GraphQL 的簡單比較。

<p>
  <img src="../images/graphQL.jpg">
</p>

REST

- 使用標準的 HTTP 方法，如 GET、POST、PUT、DELETE 來進行 CRUD 操作。
- 當你需要簡單、統一的介面來連接不同的服務/應用程式時，效果很好。
- 快取策略易於實現。
- 缺點是可能需要多次往返來組合來自不同端點的相關資料。

GraphQL

- 提供單一端點讓客戶端查詢所需的精確資料。
- 客戶端指定嵌套查詢中所需的確切欄位，伺服器返回僅包含這些欄位的最佳化負載。
- 支援修改資料的 Mutations 和即時通知的 Subscriptions
- 非常適合從多個來源聚合資料，並可以很好地滿足快速變化的前端需求
- 然而，它將複雜性轉移到客戶端，若未妥善保護，可能會允許濫用查詢。
- 快取策略可能比 REST 更複雜。

REST 和 GraphQL 之間的最佳選擇取決於應用程式和開發團隊的具體需求。GraphQL 適合複雜或頻繁變化的前端需求，而 REST 則適合需要簡單和一致的應用程式。

兩種 API 方法都不是萬能的。仔細評估需求及權衡其優劣，對於選擇正確的 API 方法非常重要。 REST 和 GraphQL 都是用於暴露資料和驅動現代應用程式的有效選擇。

### gRPC 是如何運作的？

RPC（遠端程序呼叫，Remote Procedure Call）之所以被稱為 “**遠端**” 是因為在微服務架構下，服務被部署到不同伺服器時，它允許遠端服務之間進行通訊。從使用者的角度來看，它就像是本地函數呼叫一樣。

下圖說明了 **gRPC** 的整體資料流。

<p>
  <img src="../images/grpc.jpg">
</p>

步驟 1： 從客戶端發起一個 REST 呼叫。請求主體通常是 JSON 格式。

步驟 2 - 4： 訂單服務（gRPC 客戶端）收到 REST 呼叫後，對其進行轉換，並向支付服務發起一個 RPC 請求。 gRPC 將 **客戶端 stub** 編碼為二進位格式並發送到低階傳輸層。

步驟 5： gRPC 通過 HTTP2 將封包發送到網路上。由於二進位編碼和網路優化， gRPC 被認為比 JSON 快 5 倍。

步驟 6 - 8：支付服務（gRPC 伺服器）從網路接收封包後，對其進行解碼，並調用伺服器應用程式。

步驟 9 - 11：伺服器應用程式返回结果，並將其編碼後發送到傳輸層。

步驟 12 - 14：訂單服務接收到封包後解碼，並將結果發送到客戶端應用程式。

### 什麼是 webhook？

下圖顯示了輪詢（polling）和 Webhook 的比較。

<p>
  <img src="../images/webhook.jpeg" style="width: 680px" />
</p>

假設我們經營一個電子商務網站。客戶端透過 API gateway 將訂單發送到訂單服務，然後訂單服務會將請求支付交易發送到支付服務。支付服務接著與外部支付服務供應商（payment service provider，PSP）通訊以完成交易。

處理與外部支付服務供應商（PSP）的通訊有兩種方法。

**1. 短輪詢** 

在發送支付請求到 PSP 後，支付服務不斷向 PSP 詢問支付狀態。幾輪後，PSP 終於返回狀態。

短輪詢有兩個缺點：
- 持續輪詢狀態需要消耗支付服務的資源。
- 外部服務與支付服務直接通訊，存在安全漏洞。

**2. Webhook** 

我們可以向外部服務註冊一個 webhook。這代表著：當你有請求更新的時候，通過某個 URL 對我進行回調。當 PSP 完成處理後，它會調用 HTTP 請求來更新支付狀態。

這樣就改變了程式設計法，並且支付服務不再需要浪費資源來輪詢支付狀態。

那如果 PSP 永遠不回調怎麼辦？我們可以設定一個內部定時任務，每小時檢查付款狀態。

Webhook 通常被稱為反向 API 或者推送 API，因為伺服器向客戶端發送 HTTP 請求。使用 webhook 時，我們需要注意三件事：

1. 我們需要為外部服務呼叫設計一個合適的 API。
2. 出於安全考量，我們需要在 API gateway 中設定適當的規則。
3. 我們需要在外部服務中註冊正確的 URL。

### 如何提升 API 效能？

下圖顯示了提升 API 效能的五個常見技巧。

<p>
  <img src="../images/api-performance.jpg">
</p>

分頁（Pagination）

當結果的大小很大時，這是一種常見的優化方法。結果會以類似串流的方式分片回傳給客戶端，以提高服務的回應速度。

非同步日誌記錄（Asynchronous Logging）

同步日誌記錄會在每次呼叫時處理磁碟，這會拖慢系統速度。非同步日誌記錄會先將日誌發送到無鎖緩衝區並立即返回。日誌將會被定期刷新到磁碟。這顯著減少了 I/O 開銷。

快取（Caching）

我們可以將經常訪問的資料存儲到快取中。客戶端可以先查詢快取，而不是直接訪問資料庫。如果快取未命中，客戶端可以從資料庫查詢。像 Redis 這樣的快取將資料存儲在記憶體中，因此資料訪問速度比資料庫快得多。

有效負載壓縮（Payload Compression）

請求和回應可以使用 gzip 等工具進行壓縮，這樣傳輸的資料大小會小得多。這加快了上傳和下載速度。

連接池（Connection Pool）

在訪問資源時，我們經常需要從資料庫中載入資料。開啟和關閉資料庫連接會增加顯著的開銷。因此，我們應該通過一個開放的連接池來連接資料庫。連接池負責管理連接的生命週期。

### HTTP 1.0 -> HTTP 1.1 -> HTTP 2.0 -> HTTP 3.0 (QUIC)

每一代 HTTP 都解決了什麼問題呢？

下圖說明每一代 HTTP 的主要特性。

<p>
  <img src="../images/http3.jpg" />
</p>

- HTTP 1.0 於 1996 年定稿並完整記錄。每個對於同一伺服器的請求都需要建立單獨的 TCP 連線。

- HTTP 1.1 於 1997 年發布。TCP 連線可以保持開啟以供重用（持久連線），但它無法解決 HOL（head-of-line，隊頭）阻塞問題。

  HOL 阻塞 —— 當瀏覽器允許的並行請求數用完時，後續請求需要等待前面的請求完成。

- HTTP 2.0 於 2015 年發布。通過請求複用解決了 HOL 問題，在應用層消除了 HOL 阻塞，但在傳輸層（TCP）仍然存在 HOL。

  如圖所示，HTTP 2.0 導入了 HTTP “流”的概念：這是一種抽象，允許在同一個 TCP 連線上多路複用不同的 HTTP 交換。每個流不需要依序傳送。

- HTTP 3.0 初稿於 2020 年發布。它是 HTTP 2.0 的擬議繼任者。它使用 QUIC 替代 TCP 作為底層傳輸協定，從而消除了傳輸層的 HOL 阻塞。

QUIC 基于 UDP。它將流作為傳輸層的一等公民導入。QUIC 流共享相同的 QUIC 連線，因此建立新流不需要額外的握手和慢啟動，但 QUIC 流是獨立傳送的，因此在大多數情況下，一個流的封包丟失不會影響其他流。

### SOAP vs REST vs GraphQL vs RPC

下圖說明了 API 的時間軸和 API 風格的比較。

隨著時間的推移，不同的 API 架構風格被釋出。每一種都有其標準化資料交換的模式。

你可以在圖中查看每種風格的使用案例。

<p>
  <img src="../images/SOAP vs REST vs GraphQL vs RPC.jpeg" />
</p>


### Code First vs. API First

下圖顯示了 Code First 和 API First 之間的差異。為什麼我們要考慮 API First 的設計呢？

<p>
  <img src="../images/api_first.jpg" style="width: 680px" />
</p>


- 微服務增加了系統的複雜性，我們有不同的服務來處理系統的不同功能。雖然這種架構促進了解耦和職責分離，但我們需要處理服務之間的各種溝通。

在撰寫程式碼前，最好先考慮系統的複雜性並仔細定義服務的邊界。

- 不同的功能團隊需要對功能的理解等方面溝通一致，而專門的功能團隊只負責自己的組件和服務。建議組織透過 API 設計確保溝通上的一致。

在撰寫程式碼前，我們可以模擬請求和回應來驗證 API 設計。

- 提高軟體質量和開發者生產力。由於在項目開始時已經解決了大部分不確定性因素，因此整體開發過程會更加順利，軟體質量也會得到很大的提升。

開發者也會對這個過程感到满意，因為他們可以專注於功能開發，而不用應對突如其來的變更。

在項目生命周期結束時出現意外的可能性會降低。

因為我們先設計了 API，所以在編寫程式碼的同時可以設計測試。在某種程度上，我們在使用 API First 開發時，同時也可以有 TDD（測試驅動開發）。

### HTTP 狀態碼

<p>
  <img src="../images/http-status-code.jpg" style="width: 540px" />
</p>

HTTP 狀態碼分為五個類別：

- 訊息（Informational） (100-199)
- 成功（Success） (200-299)
- 重新導向（Redirection） (300-399)
- 客戶端錯誤 (400-499)
- 伺服器錯誤 (500-599)

### API Gateway 有什麼作用？

下圖顯示了詳細資訊。

<p>
  <img src="../images/api_gateway.jpg" style="width: 520px" />
</p>

步驟 1 - 客戶端發送 HTTP 請求到 API Gateway。

步驟 2 - API Gateway 解析並驗證 HTTP 請求中的屬性。

步驟 3 - API Gateway 執行允許列表/拒絕列表檢查。

步驟 4 - API Gateway 與 身份提供商 進行身份驗證和授權。

步驟 5 - 對請求應用速率限制規則，如果超過限制，請求將被拒絕。

步驟 6 和 7 - 現在請求已通過基本檢查，API Gateway 通過路徑匹配將請求路由到相關服務。

步驟 8 - API Gateway 將請求轉換為適當的協定並發送到後端微服務。

步驟 9-12: API Gateway 可以妥善處理錯誤，並在錯誤需要較長時間恢復時處理故障（斷路器）。它還可以利用 ELK (Elastic-Logstash-Kibana) 堆疊進行日誌記錄和監控。有時，我們還會在 API Gateway 中緩存資料。

### 我們要如何設計高效安全的 API？

下圖用購物車的例子，顯示了典型的 API 設計。

<p>
  <img src="../images/safe-apis.jpg" />
</p>

注意，API 設計不僅僅是 URL 路徑設計。大多數情況下，我們需要選擇合適的資源名稱、識別符和路徑模式。設計合適的 HTTP 標頭字段或設計高效的 API Gateway 限速規則同樣重要。

### TCP/IP 封裝

資料是如何在網路上傳輸的？為什麼我們需要 OSI 模型中的這麼多層？

下圖顯示了資料在網路傳輸過程中的封裝和解封裝過程。

<p>
  <img src="../images/osi model.jpeg" />
</p>

步驟 1：當裝置 A 通過 HTTP 協定向裝置 B 傳送資料時，首先在應用層增加 HTTP 標頭。

步驟 2：然後在資料上增加 TCP 或 UDP 標頭。它在傳輸層被封裝成 TCP 段。標頭包含源通訊埠、目标通訊埠和序列號。

步驟 3：接著在網路層將段封裝成 IP 標頭。IP 標頭包含源/目的 IP 地址。

步驟 4：IP 在資料連結層，向資料報新增 MAC 標頭，其中包含源/目的 MAC 地址。

步驟 5：封裝後的幀被送到實體層，並以二進位位元形式在網路上傳輸。

步驟 6-10：當裝置 B 從網路接收到位元時，它執行解封裝過程，這是封裝過程的反向處理。當標頭逐層被移除，最終裝置 B 可以讀取到資料。

網路模型中之所以需要層的概念，是因為每一層都專注於自己的職責。每一層可以依賴標頭進行處理指令，而不需要知道上一層資料的含義。

### 為什麼 Nginx 被叫做「反向」代理？

下圖顯示了正向代理（𝐟𝐨𝐫𝐰𝐚𝐫𝐝 𝐩𝐫𝐨𝐱𝐲）和反向代理（𝐫𝐞𝐯𝐞𝐫𝐬𝐞 𝐩𝐫𝐨𝐱𝐲）的差別。

<p>
  <img src="../images/Forward Proxy v.s. Reverse Proxy2x.jpg" style="width: 720px" />
</p>

正向代理指的是位於用戶裝置和網路之間的伺服器。

正向代理通常用於：

1. 保護客戶端
2. 規避瀏覽限制
3. 阻止存取某些內容

反向代理是一個接受客戶端請求後將請求轉發到網頁伺服器，並將結果返回給客戶端的伺服器，就像是代理伺服器處理了請求一樣。

反向代理適用於：

1. 保護伺服器
2. 負載平衡
3. 快取靜態內容
4. 加密和解密 SSL 通訊

### 常見的負載平衡演算法有哪些？

下圖顯示了六種常見的演算法。

<p>
  <img src="../images/lb-algorithms.jpg" />
</p>

- 靜態演算法

1. 輪詢

   客戶端請求依序發送到不同的服務。這些服務通常需要是無狀態的。

2. 黏性輪詢

   這是輪詢演算法的改進版。如果 Alice 的第一個請求發送到服務 A，那麼後續的請求也會發送到服務 A。

3. 加權輪詢

   管理員可以為每個服務指定權重。權重較高的服務處理更多的請求。

4. 雜湊值

   這個演算法對進入的請求的 IP 或 URL 套用雜湊函數。請求根據雜湊函數的結果路由到相關的實例。

- 動態演算法

1. 最少連線數

   新的請求會發送到連線數最少的服務實例。

2. 最短回應時間

   新的請求會發送到回應時間最快的服務實例。

### URL，URI，URN - 你知道它們的區別嗎？

下圖顯示了 URL、URI 和 URN 的比较。

<p>
  <img src="../images/url-uri-urn.jpg" />
</p>

- URI

URI 代表統一資源識別碼（Uniform Resource Identifier）。它識別網路上的邏輯或物理資源。URL 和 URN 是 URI 的子類型。URL 定位資源，而 URN 命名資源。

URI 由以下部分組成：
scheme:[//authority]path[?query][#fragment]

- URL

URL 代表統一資源定位符（Uniform Resource Locator），是 HTTP 的關鍵概念。它是網路上唯一資源的地址。它也可以與其他協定如 FTP 和 JDBC 一起使用。

- URN

URN 代表統一資源名稱（Uniform Resource Name）。它使用 urn 協定。URN 不能用來定位資源。圖中給出的簡單例子由命名空間和命名空間特定的字串組成。

如果你想了解更多詳細資訊，我建議參考 [W3C 的說明](https://www.w3.org/TR/uri-clarification/)。

## CI/CD

### 簡單解釋 CI/CD Pipeline

<p>
  <img src="../images/ci-cd-pipeline.jpg" style="width: 680px" />
</p>

第一部分 - SDLC 與 CI/CD

軟體開發生命週期（software development life cycle，SDLC）包含幾個關鍵階段：開發、測試、部署和維護。CI/CD 自動化與整合這些階段，以實現更快且更可靠的發佈。

當程式碼推送到 git Repo 時，它會觸發自動化的建置和測試過程。端到端 (e2e) 測試案例會執行以驗證程式碼。如果測試通過，程式碼可以自動部署到預備（staging）/ 生產（production）環境。如果發現問題，程式碼會被送回開發階段進行錯誤修復。這種自動化為開發人員提供了快速反饋，並減少了生產環境中出現錯誤的風險。

第二部分 - CI 和 CD 的區別

持續整合 (Continuous Integration，CI) 自動化建置、測試和合併過程。每當程式碼提交時，它都會運行測試，以便及早檢測整合問題。這鼓勵頻繁的程式碼提交和快速反饋。

持續交付 (Continuous Delivery，CD) 自動化發佈過程，如基礎設施變更和部署。它確保軟體可以隨時通過自動化工作流程可靠地發佈。CD 也可以自動化生產部署前所需的手動測試和批准步驟。

第三部分 - CI/CD Pipeline

一個典型的 CI/CD Pipeline 有幾個連接的階段：
- 開發者將程式碼變更提交到版本控制系統
- CI 伺服器檢測到變更並觸發建置
- 程式碼被編譯並測試（單元測試，整合測試）
- 測試結果報告給開發者
- 一旦成功後，就會將其部署到預備環境
- 在發佈前可能會在預備環境進行進一步測試
- CD 系統將批准的變更部署到生產環境

### Netflix 技術堆疊（CI/CD Pipeline）

<p>
  <img src="../images/netflix-ci-cd.jpg" style="width: 720px" />
</p>

規劃：Netflix 團隊使用 JIRA 進行規劃，並使用 Confluence 進行文件記錄。

編碼：Java 是後端服務的主要程式語言，其他語言則用於不同的使用情境。

建置：主要使用 Gradle 進行建置，並建立 Gradle 插件以支援各種使用情境。

封裝：將套件和相依性打包成 Amazon Machine Image (AMI) 以供發佈。

測試：測試強調生產文化，專注於建立混沌工具（chaos tool）。

部署：Netflix 使用自建的 Spinnaker 進行金絲雀部署（canary rollout deployment）。

監控：監控指標集中在 Atlas 中，並使用 Kayenta 來檢測異常。

事件報告：事件根據優先級進行分派，並使用 PagerDuty 來處理事件。

## 架構模式

### MVC、MVP、MVVM、MVVM-C 和 VIPER

這些架構模式是應用程式開發中最常用的模式，不論是在 iOS 還是 Android 平台。開發人員導入它們來克服早期模式的限制。那麼，它們有什麼不同呢？

<p>
  <img src="../images/client arch patterns.png" style="width: 720px" />
</p>

- MVC，最古老的模式，最早可追溯到將近 50 年前
- 每個模式都有一個 "View" (V)，負責顯示內容和接收使用者輸入
- 大部分的模式都包含一個 "Model" (M) ，用於管理業務資料
- "Controller" 、 "Presenter" 和 "View-Model" 是介於 View 和 Model 之間的轉換器 (在 VIPER 模式中是 "Entity" ）。

### 每一位開發者都應該知道的 18 種關鍵設計模式

設計模式是常見設計問題的可重複使用解決方案，能夠使開發過程更加順暢和高效。它們是構建更好軟體結構的藍圖。以下是一些最流行的模式：

<p>
  <img src="../images/18-oo-patterns.png" />
</p>

- 抽象工廠（Abstract Factory）模式：族群建立者 - 建立一組或多组相關對象。
- 建造者（Builder）模式：樂高大師 —— 逐步構建物件，分離建立和外觀。
- 原型（Prototype）模式：克隆製造者 —— 建立完備實體的副本。
- 單例（Singleton）模式：唯一實體 ——  只有一個實體的特殊類別。
- 適配器（Adapter）模式：萬能插頭 —— 連接不同介面的事物。
- 橋接（Bridge）模式：功能連接器 —— 連接物件的工作方式和它的作用。
- 複合（Composite）模式：樹形建構器 —— 形成簡單和複雜部分的樹狀結構。
- 裝飾者（Decorator）模式：定制者 —— 在不改變核心的情況下為物件新增功能。
- 門面（Facade）模式：一站式服務 ——通過單一簡化介面來代表整個系統。
- 享元（Flyweight）模式：節約空間小幫手 —— 高效共享小型可重用項目。
- 代理（Proxy）模式：替身演員 —— 代表另一個物件，控制存取或操作。
- 責任鏈（Chain of Responsibility）模式：請求中繼 —— 將請求通過一系列物件傳遞，直至被處理。
- 指令（Command）模式：任務包裝器 —— 將請求轉化為一個準備就緒的物件。
- 迭代器（Iterator）模式：集合探索者 —— 逐個存取集合中的元素。
- 中介者（Mediator）模式：通訊中心 —— 簡化不同類別之間的互動。
- 備忘錄（Memento）模式：時間膠囊 —— 捕捉並恢復物件狀態。
- 觀察者（Observer）模式：新聞廣播員 —— 通知類別其他物件的變更。
- 訪問者（Visitor）模式：熟練的訪客 —— 為類別增加新操作而不對其進行更改。

## 資料庫

### 關於雲端服務中不同類型的資料庫的一個方便速查表

<p>
  <img src="../images/cloud-dbs2.png" />
</p>

为你的项目选择正确的資料庫是一项复杂的任务。许多資料庫选项都有各自的适用场景，互不重复，这很容易导致决策疲劳。

我们希望这份速查表能够提供高层次的指导，以帮你找到符合项目需求的正确服务，并避免潜在陷阱。

注意：Google 关于其資料庫用例的文件有限。尽管我们尽力檢視可用的内容并得出最佳选择，但某些条目可能需要更加准确。

### 8 種支援資料庫的資料結構

根据使用场景不同，答案也不同。数据可以在記憶體或磁碟上建立索引。同样，数据格式也各不相同，例如数字、字符串、地理坐标等。系统可能是写入密集型的，也可能是读取密集型的。所有这些因素都会影响您对資料庫索引格式的选择。

<p>
  <img src="../images/8-ds-db.jpg" />
</p>

下面是一些用于索引数据的最流行的資料結構：

- 跳跃表（Skiplist）：常见的記憶體索引类型。在 Redis 中使用
- 哈希索引（Hash index）：“Map” 資料結構（或者“Collection”）的一个非常常见的实现
- SSTable：不可变的磁碟 “Map” 实现
- LSM 树：Skiplist + SSTable。高写入吞吐量
- B 树（B-tree）：基于磁碟的方案。一致读写性能
- 倒排索引（Inverted index）：用于文件索引。在 Lucene 中使用
- 后缀树（Suffix tree）：用于字符串模式搜索
- R 树（R-tree）多维搜索，例如寻找最近邻

### 一行 SQL 語法在資料庫中是如何執行的？

下图显示了 SQL 语句的执行过程。注意，不同資料庫的架構不一样，下图演示的是一些常见设计。

<p>
  <img src="../images/sql execution order in db.jpeg" style="width: 580px" />
</p>


步骤 1 - 通过传输层協定（例如，TCP）将 SQL 语句发送到資料庫。

步骤 2 - 发送 SQL 语句到指令解析器，然后指令解析器对其进行语法和语义分析，生成查询树。

步骤 3 - 发送查询树到优化器。优化器创建执行计划。

步骤 4 - 发送执行计划到执行器。执行器根据执行检索数据。

步骤 5 - 存取方法提供执行所需的数据获取逻辑，从存储引擎检索数据。

步骤 6 - 存取方法决定 SQL 语句是否唯讀。如果是唯讀查询（SELECT 语句），就会将其传到缓冲区管理器以进行进一步处理。缓冲区管理器在快取或者数据文件中查询数据。

步骤 7 - 如果是 UPDATE 或者 INSERT 语句，则将其传到事务管理器进行进一步处理。

步骤 8 - 事务期间，数据处于锁定模式。这由锁管理器保证。它还确保事务的 ACID 属性。

###  CAP 理論

CAP 理論是计算机科学中最著名的术语之一，但我打赌，不同的开发者对其有不同的理解。让我们来看看它是什么，以及為什麼它会令人困惑。

<p>
  <img src="../images/cap theorem.jpeg" />
</p>

CAP 理論指出，分散式系统不能同时提供这三个保证中的两个以上的保证。

**一致性（Consistency）**：一致性意味着，不管客户端连接到哪个节点，它们都同时看到相同的数据。

**可用性（Availability）**：可用性意味着，即使某些节点发生了故障，任何客户端请求都能得到响应。

**分区容错性（Partition Tolerance）**：分区表示两个节点之间的通信发生了中断。分区容错性意味着，尽管存在網路分区，系统仍能继续运行。

“三分之二”表述可能有用，**但这种简化可能会产生误导**。

1. 选择合适的資料庫并不容易。仅仅根据 CAP 定理来证明我们的选择并不够。例如，公司不会只因为 Cassandra 是一个 AP 系统就选择它作为聊天应用。Cassandra 具有一系列不错的特性，使其成为存储聊天消息的理想选择。我们需要更深入地挖掘。

2. “CAP 仅限制了一小部分的设计空间：在存在分区的情况下实现完美的可用性和一致性是很少见的”。引自论文：十二年后的 CAP：“规则”是如何改变的（CAP Twelve Years Later: How the “Rules” Have Changed）。

3. 该理論是关于百分百可用性和一致性的。更现实的讨论是在没有網路分区的情况下，延迟和一致性之间的权衡。详情请参阅 PACELC 定理。

**CAP 理論真的有用吗？**

我认为它依然有用，因为它让我们能够进行一系列权衡讨论，但这只是故事的一部分。在选择正确的資料庫时，我们需要更深入挖掘。

### 記憶體和儲存的類型

<p>
  <img src="../images/Types_of_Memory_and_Storage.jpeg" style="width: 420px" />
</p>


### 視覺化 SQL 查询

<p>
  <img src="../images/sql-execution-order.jpg" style="width: 580px" />
</p>

SQL 语句由数据系统执行，包含以下几个执行步骤：

- 解析 SQL 语句并检查其有效性
- 将 SQL 语句转化为内部表达形式，例如，关系代数
- 优化内部表达形式，并创建利用索引信息的执行计划
- 执行计划并返回结果

SQL 的执行是非常复杂的，涉及很多考虑因素，例如：

- 索引和快取的使用
- 表连接的顺序
- 并发控制
- 事务管理

### SQL 語言

1986 年，SQL (Structured Query Language，结构化查询語言) 成为标准。在接下来的 40 年间，它成为了关系資料庫管理系统的主导語言。阅读最新标准（ANSI SQL 2016）可能会耗费你大量的时间。那么，我要怎样才能学习它呢？

<p>
  <img src="../images/how-to-learn-sql.jpg" />
</p>

SQL 語言有五个组件：

- DDL：数据定义語言，例如 CREATE、ALTER、DROP
- DQL：数据查询語言，，例如 SELECT
- DML：数据操作語言，例如 INSERT、UPDATE、DELETE
- DCL：数据控制語言，例如 GRANT、REVOKE
- TCL：事务控制語言，例如 COMMIT、ROLLBACK

对于一个后端工程师来说，你可能需要了解上面大多数组件。而作为一名数据分析师，你可能需要很好地了解 DQL。根据需求，选择与自己关系最大的主题吧。


## 快取

### 快取無所不在

下图说明了在典型架構中，我们快取数据的位置。

<p>
  <img src="../images/where do we cache data.jpeg" style="width: 720px" />
</p>

在这个架構中，有**多个层**。

1. 客户端应用：HTTP 响应可以由浏览器进行快取。我们第一次通过 HTTP 请求数据，数据返回时在 HTTP 标头中包含过期策略；当我们再次请求数据时，客户端应用会先尝试从浏览器快取中检索数据。
2. CDN：CDN 快取静态網路资源。客户端可以就近从 CDN 节点检索数据。
3. 負載平衡器：負載平衡器也可以快取资源。
4. 消息传递基础设施（Messaging infra）：消息代理首先将消息存储在磁碟上，然后消费者按需检索消息。根据保留策略（retention policy），数据会在 Kafka 集群中快取一段时间。
5. 服务：服务存在多层快取。如果数据没有快取在 CPU 快取中，那么服务会尝试从記憶體中检索数据。有时，服务会有二级快取，来将数据存储到磁碟中。
6. 分散式快取：像 Redis 这样的分散式快取在記憶體中保存多个服务的键值对。和資料庫相比，它能提供更好的读/写性能。
7. 全文搜索：有时，我们需要使用像 Elastic Search 这样的全文搜索来对文件或日志进行搜索。因此，搜索引擎中也会对数据副本进行索引。
8. 資料庫：即使在資料庫中，我们也有不同级别的快取：
- WAL(Write-ahead Log)：在构建 B 树索引前，先将数据写入 WAL
- Bufferpool：一块記憶體区域，分配于快取查询结果
- 物化視圖（Materialized View）：预计算查询结果并将其存储在資料庫表中，以获得更好的查询性能
- 事务日志：记录所有事务和資料庫更新
- 复制日志：用于记录資料庫集群中的复制状态

### 為什麼 Redis 這麼快？

主要有三个原因，如下图所示。

<p>
  <img src="../images/why_redis_fast.jpeg" />
</p>


1. Redis 是一个基于 RAM 的数据存储。RAM 存取至少比随机磁碟存取快 1000 倍。
2. Redis 利用 IO 多路复用和单线程执行循环来提高执行效率。
3. Redis 利用多种高效的底层資料結構。

问题：另一种流行的記憶體存储是 Memcached。你知道Redis和Memcached的区别吗？

> 译者注：答案可以参考 [redis和memcached的区别和使用场景](https://cloud.tencent.com/developer/article/1692015)

您可能已经注意到该图的风格与我之前的帖子不同。请告诉我您更喜欢哪一个。

### Redis 的使用場景

<p>
  <img src="../images/top-redis-use-cases.jpg" style="width: 520px" />
</p>

Redis 不仅仅是快取。

Redis 可用于多种场景，如图所示。

- 会话（Session）

  我们可以使用 Redis 在不同服务之间共享用户会话数据。

- 快取（Cache）

  我们可以使用 Redis 来快取对象或页面，尤其是热点数据。

- 分散式锁

  我们可以使用 Redis 字符串来获取分散式服务之间的锁。

- 计数器（Counter）

  我们可以用它来统计文章的点赞数或阅读量。

- 速率限制器（Rate limiter）

  我们可以对某些用户 IP 应用速率限制器。

- 全局 ID 生成器（Global ID generator）

  我们可以使用 Redis Int 作为全局 ID。

- 购物车（Shopping cart）

  我们可以使用 Redis Hash 来表示购物车中的键值对。

- 计算用户留存率

  我们可以使用 Bitmap 来表示用户每天的登录情况并计算用户留存情况。

- 消息佇列

  我们可以使用 List 作为消息佇列。

- 排行（Ranking）

  我们可以使用 ZSet 对文章进行排序。

### 最佳快取策略

设计大型系统通常需要仔细地考虑快取。下面是五种常用的快取策略。

<p>
  <img src="../images/top_caching_strategy.jpeg" style="width: 680px" />
</p>



## 微服務架構

### 典型的微服務架構是什麼樣的？

<p>
  <img src="../images/typical-microservice-arch.jpg" style="width: 520px" />
</p>

上图显示了一个典型的微服務架構。

- 負載平衡器（Load Balancer）：它将传入的流量分发到多个后端服务。
- CDN (Content Delivery Network，内容分发網路)：CDN 是一组地理分布的服务器，用于保存静态内容以实现更快的传输。客户端首先在 CDN 查找内容，然后再进行后端服务。
- API 网关（API Gateway）：它处理进来的请求并将其路由到相关服务。它与身份提供者和服务发现进行通信。
- 身份提供者（Identity Provider）：负责处理用户的身份验证和授權。
- 服务註冊和发现（Service Registry & Discovery）：该组件负责微服務註冊和发现，此外，API 网关从此组件查找相关服务进行通信。
- 管理（Management）：该组件负责监控服务。
- 微服務：根据域不同来设计和部署微服務。每个域都有其自身的資料庫。API 网关通过 REST API 或者其他協定与微服務进行通信，同一个域中的微服務使用 RPC （遠端过程调用）相互通信。

微服務的优点：

- 可以对其进行快速设计、部署和水平扩展。
- 每个域都可以由专门的团队独立维护。
- 可以在每个域对业务需求进行定制，从而获得更好的支持。

### 微服務最佳實踐

一图胜千言：开发微服務的 9 个最佳实践。

<p>
  <img src="../images/microservice-best-practices.jpeg" />
</p>

开发微服務时，我们需要遵循以下最佳实践：

1. 为每个微服務使用单独的数据存储
2. 保持代码处于相似的成熟度
3. 单独构建每个微服務
4. 为每个微服務分配单一职责
5. 部署到容器中
6. 设计无状态服务
7. 采用领域驱动设计
8. 设计微前端
9. 编排微服務

### 微服務通常使用哪些技術堆疊？

下面，你将看到一张显示微服務技術堆疊的图标，同时涉及开发阶段和生产阶段。

<p>
  <img src="../images/microservice-tech.jpeg" />
</p>


▶️ 预生产（𝐏𝐫𝐞-𝐏𝐫𝐨𝐝𝐮𝐜𝐭𝐢𝐨𝐧）

- 定义 API - 这为前后端之间建立契约。为此，我们可以使用 Postman 或者 OpenAPI。
- 开发 - Node.js 或 react 在前端开发中很是流行，而 java/python/go 则是后端开发的流行之选。此外，我们需要根据 API 定义更改 API 网关的配置。
- 持续集成 - JUnit 和 Jenkins 用于自动化测试。打包代码到 Docker 镜像并部署为微服務。

▶️ 生产（𝐏𝐫𝐨𝐝𝐮𝐜𝐭𝐢𝐨𝐧）

- NGinx 是負載平衡的常见选择。Cloudflare 则提供 CDN (Content Delivery Network)功能。
- API 网关 - 我们可以使用 spring boot 作为网关，并 Eureka/Zookeeper 进行服务发现。
- 在云上部署微服務。可以选择 AWS、Microsoft Azure 或者 Google GCP。快取和全文搜索 —— 通常选择 Redis 来快取键值对。使用 Elasticsearch 进行全文搜索。
- 通信 - 为了使服务之间能够相互通信，我们可以使用 Kafka 或者 RPC。
- 持久化 - 可以使用 MySQL 或者 PostgreSQL 作为关系資料庫，使用 Amazon S3 作为对象存储。如有必要，我们还可以使用 Cassandra 进行宽列存储。
- 管理和监控 - 为了管理如此多的微服務，常见的运维攻击包括 Prometheus、Elastic Stack 和 Kubernetes。

### 為什麼 Kafka 那麼快？

有许多设计决策为 Kafka 的性能做出了贡献。在这里，我们将关注其中两个设计决策。我们认为这两者最有分量。

<p>
  <img src="../images/why_is_kafka_fast.jpeg" />
</p>

1. 第一个是 Kafka 对顺序 I/O 的依赖。
2. 赋予 Kafka 性能优势的第二个设计决策是它对于效率的关注：零拷贝原则（zero copy principle）。

上图说明了数据是如何在生产者和消费者之间传输的，以及零拷贝的含义。

- 步骤 1.1 - 1.3：生产者将数据写到磁碟中
- 步骤 2：消费者无需零拷贝即可读取数据。

    * 2.1 从磁碟中将数据載入到操作系统快取

    * 2.2 从操作系统快取拷贝数据到 Kafka 应用

    * 2.3 Kafka 应用拷贝数据到 socket 快取

    * 2.4 从 socket 快取拷贝数据到网卡

    * 2.5 网卡发送数据给消费者


- 步骤 3：消费者以零拷贝方式读取数据

    * 3.1 从磁碟載入数据到操作系统快取
    * 3.2 操作系统快取通过 sendfile() 指令，直接将数据拷贝到网卡
    * 3.3 网卡发送数据给消费者

零拷贝（Zero copy）是一种在應用程式上下文和内核上下文之间保存多个数据副本的快捷方式。

## 支付系統

### 如何學習支付系統？

<p>
  <img src="../images/learn-payments.jpg" />
</p>

### 為什麼信用卡被稱為「銀行最賺錢的產品」？VISA/萬事達是如何賺錢的？

下图显示了信用卡支付流程背后的经济学。

<p>
  <img src="../images/how does visa makes money.jpg" style="width: 640px" />
</p>

1. 持卡人（cardholder）向商家（merchant）支付 100 美元以购买产品。

2. 商家从使用量较高的信用卡中获益，并且需要为发卡机构和卡網路（card network）提供的支付服务进行补偿。收单银行（acquiring bank）向商家收取一定费用，称为“商家折扣费”。

3 - 4. 收单银行保留 0.25 美元作为收单加价，并向发卡行（issuing bank）支付 1.75 美元作为互换费。商户折扣费应该覆盖互换费用。

互换费用由卡網路设定，因为每个商户与每个发卡行就费用进行谈判效率较低。

1. 卡網路与各银行建立網路评估和费用，银行每月支付卡網路服务费。例如，VISA 对每次刷卡收取 0.11% 的评估费，另加 0.0195 美元的使用费。

2. 持卡人向发卡行支付其服务费。

发卡行为何需要获得补偿呢？

- 即使持卡人未能向发卡行支付款项，发卡行仍需支付商家。
- 发卡行在持卡人向其支付之前就已支付商家。
- 发卡行有其他运营成本，包括管理客户账户、提供对账单、欺诈检测、风险管理、清算等。

### 當我們在店家刷卡時，VISA 是如何運作的？

<p>
  <img src="../images/visa_payment.jpeg" />
</p>


VISA、Mastercard 和 American Express 充当资金清算和结算的卡網路。收单银行和发卡行可能（而且通常是）不同。如果银行要在没有中介的情况下一笔一笔地结算交易，那么每家银行都必须与所有其他银行结算交易。这是相当低效的。

上图显示了 VISA 在信用卡支付流程中的角色。涉及两个流程。当客户刷信用卡时就会发生授權流程（authorization flow）。当商家想要在一天结束时拿到钱时，就会发生捕获和结算流程（capture and settlement flow）。

- 授權流程

步骤 0：发卡行向其客户发放信用卡。

步骤 1：持卡人想购买产品，于是在商家店铺的销售点（POS）终端上刷信用卡。

步骤 2：POS 终端将交易发送给提供该POS终端的收单银行。

步骤 3 和 4：收单银行将交易发送到卡網路（也称为卡方案）。然后卡網路将交易发送到发卡行以获取审批。

步骤 4.1，4.2 和 4.3：如果交易得到批准，发卡行会冻结资金。发送批准或拒绝的信息到收单银行和POS终端。

- 捕获和结算流程

步骤 1 和 2：商家希望在一天结束时收到款项，因此在POS终端上点击“捕获（capture）”。交易被批量发送到收单银行。收单银行会将带有交易的批处理文件发送到卡網路。

步骤 3：卡網路对从不同收单银行收集的交易进行清算，并将清算文件发送到不同的发卡行。

步骤 4：发卡行确认清算文件的正确性，并将资金转移给相关的收单银行。

步骤 5：收单银行然后将资金转移给商家的银行。

步骤 4：卡網路清理来自不同收单银行的交易。清算是一个互相抵消交易的过程，从而减少总交易数。

在此过程中，卡網路承担了与每家银行交涉的重任，并得到了服务费作为回报。

### 世界各地的支付系統系列（第一部分）：印度的統一支付介面（Unified Payments Interface，UPI）


什麼是 UPI？UPI 是由印度国家支付公司开发的即时实时支付系統。

它占当今印度数字零售交易的 60%。

UPI = 支付标记語言（payment markup language） + 可互操作支付标准（standard for interoperable payments）


<p>
  <img src="../images/how-does-upi-work.png"  style="width: 600px" />
</p>


## DevOps

###  DevOps vs. SRE vs. 平台工程（Platform Engineering）。有何不同？

DevOps、SRE 和平台工程的概念是在不同时间出现的，并由不同的个人和组织开发。

<p>
  <img src="../images/devops-sre-platform.jpg" />
</p>

DevOps 的概念是 Patrick Debois 和 Andrew Shafer 于 2009 年在敏捷大会上提出的。他们试图通过促进对整个软件开发生命周期的协作文化和共同责任，来弥合软件开发和运维之间的差距。

SRE（Site Reliability Engineering，站点可靠性工程）由谷歌在 2000 年代初首创，用以解决管理大规模复杂系统的运维挑战。谷歌开发了 SRE 实践和工具，例如 Borg 集群管理系统和 Monarch 监控系统，来提高其服务的可靠性和效率。

平台工程则是一个较新的概念，构建在 SRE 工程的基础上。平台工程的确切起源未明，但通常认为它是 DevOps 和 SRE 实践的延伸，专注于提供一个产品开发的综合平台，来支持整个业务视角。

值得注意的是，虽然这些概念是在不同时期出现的，它们都与改善软件开发和运营中的协作、自动化和效率的更广泛趋势息息相关。

### k8s（Kubernetes）是什么？

K8s 是一个容器编排系统。用于容器部署和管理。其设计很大程度上受到 Google 内部系统 Borg 的影响。

<p>
  <img src="../images/k8s.jpeg" style="width: 680px" />
</p>

一个 Kubernetes（k8s）集群由一组称为节点（node）的工作机器组成，这些节点上运行着容器化應用程式。每个集群至少有一个工作节点（worker node）。

工作节点托管 Pod，也就是应用工作负载的组件。控制平面（control plane）负责管理集群中的工作节点和Pod。在生产环境中，控制平面通常跨多台计算机运行，而一个集群通常运行多个节点，提供容错性和高可用性。

- 控制平面组件（Control Plane Components）

1. API 服务器（API Server）

   API 服务器与 k8s 集群中的所有组件通信。Pod 上的所有操作都是通过与 API 服务器通信来执行的。

2. 调度器（scheduler）

   调度器监控 Pod 工作负载，并给新创建的 Pod 分配负载。

3. 控制器管理器（controller manager）

   控制器管理器运行控制器，包括节点控制器（Node Controller）、作业控制器（Job Controller）、EndpointSlice 控制器（ EndpointSlice Controller）和 ServiceAccount 控制器（ServiceAccount Controller）。

4. Etcd

   etcd 是一个键值存储，用作 Kubernetes 所有集群数据的后备存储。

- 节点（Node）

1. Pod

   一个 Pod 是一组容器，也是 k8s 管理的最小单元。每一个 Pod 都有一个单独的 IP 地址，Pod 中的每一个容器共享这个 IP 地址。

2. Kubelet

   集群中每个节点上都运行的代理。它保证了容器在 Pod 中运行。

3. Kube Proxy

   Kube-proxy 是一个網路代理，它运行在集群中的每一个节点上。它路由来自服务的流量到节点。它还将工作请求转发到正确的容器中。

### Docker vs. Kubernetes。我们应该用哪一个？

<p>
  <img src="../images/docker-vs-k8s.jpg" style="width: 680px" />
</p>


Docker 是什么？

Docker 是一个开源平台，允许您打包、分发以及在隔离的容器中运行应用。它专注于容器化，提供封裝了应用及其依赖的轻量级环境。

Kubernetes 是什么？

Kubernetes，通常称为 K8s，是一个开源的容器编排平台。它提供了一个框架，用于自动化部署、扩展、以及管理跨节点集群中的容器化应用。

它们两者之间有什么区别呢？

Docker：Docker 在单个操作系统主机上的单个容器级别上运行。

您必须手动管理每个主机，而为多个相关容器设置網路、安全策略和存储可能会变得复杂。

Kubernetes：Kubernetes 在集群级别上运行。它管理跨多个主机的多个容器化應用程式，提供任务（如负载平衡、扩展）自动化，并确保應用程式所需状态。

简而言之，Docker 专注于容器化和在单个主机上运行容器，而 Kubernetes 则专注于跨主机集群大规模管理和编排容器。

### Docker 的工作原理

下图显示了 Docker 的架構，以及当我们运行了“docker build”、“docker pull”和“docker run”时，它是如何運作的。

<p>
  <img src="../images/docker.jpg" style="width: 680px" />
</p>

Docker 架構中有 3 个组件：

- Docker 客户端

  Docker 客户端与 Docker daemon 通信。

- Docker 主机

  Docker daemon 监听 Docker API 请求，管理 Docker 对象，例如镜像（image）、容器、網路和卷。

- Docker registry

  Docker registry 存储 Docker 镜像。Docker Hub 是一个人和人都可以使用的公共镜像存储库。

让我们以“docker run” 指令为例。

1. Docker 从 registry 拉取镜像。
2. Docker 创建一个新的容器。
3. Docker 为容器分配一个读写文件系统。
4. Docker 创建一个網路介面，来将容器连接到預設網路上。
5. Docker 启动容器。

## GIT

### Git 指令是如何運作的？

首先，确定代码存储在何处是至关重要的。通常假设只有两个地方 —— 一份代码在像 Github 这样的遠端服务器上，而另一份则在我们的本地机器上。然而，这不完全正确。Git 在我们的机器上维护了三份本地存储，这意味着，我们的代码可以在四个地方找到：

<p>
  <img src="../images/git-commands.png" style="width: 600px" />
</p>


- 工作目錄（Working directory）：我们编辑文件的地方
- 暂存区（Staging area）：一个临时区域，代码保存在此处，以备下一次提交
- 本地仓库（Local repository）：包含已提交的代码
- 遠端仓库（Remote repository）：存储代码的遠端服务器

大多数的 Git 指令主要在这四个位置之间移动文件。

### Git 的工作原理

下图显示了 Git 的工作流程。

<p>
  <img src="../images/git-workflow.jpeg" style="width: 520px" />
</p>


Git 是一个分散式版本控制系统。

每一位开发者都维护了主仓库的一份本地拷贝，他们编辑以及提交到这个本地拷贝中。

提交操作是非常快的，因为此操作并不与遠端仓库进行交互。

如果遠端仓库挂了，可以从本地仓库恢复文件。

### Git merge vs. Git rebase

有何不同？

<p>
  <img src="../images/git-merge-git-rebase.jpeg" style="width: 680px" />
</p>


当我们将一个 Git 分支的**更改合并**到另一个分支时，我们可以使用“git merge” 或者“git rebase”。下图显示了两个指令的工作原理。

**Git merge**

这在主分支创建了一个新的提交 G’。G’ 将主分支和特性分支的历史记录连接在一起。

Git merge 是**非破坏性的**。主分支和特性分支都不会被修改。

**Git rebase**

Git rebase 将特性分支的历史记录移动到主分支的头部。它为特性分支中的每次提交，分别创建新的提交 E’、F’ 和 G’。

rebase 的好处是，通过它，我们可以拥有一个线性的**提交历史记录**。

如果不遵循“git rebase 的黄金法则”，rebase 就有可能是一种危险操作。

**git rebase 的黄金法则**

永远不要在公共分支上使用它！

## 雲端服務

### 不同雲端服務的便捷速查表（2023 年版本）

<p>
  <img src="../images/cloud-compare.jpg" />
</p>


### 什麼是雲端原生（cloud native）？

下图显示了自 20 世纪 80 年代以来架構和流程的演变。

<p>
  <img src="../images/cloud-native.jpeg" style="width: 640px" />
</p>

通过使用雲端原生技术，组织可以在公有云、私有云和混合云上构建和运行可扩展的應用程式。

这意味着应用被设计成能够利用云功能，因此，它们具有负载弹性，并且易于扩展。

雲端原生包含 4 个方面：

1. 开发流程

   它已经从瀑布流发展到敏捷，再到 DevOps。

2. 应用架構

   架構已经从單體架構演变为微服務。每个服务都被设计得很小，从而适应云容器中的有限资源。

3. 部署和打包

   过去，应用被部署到物理服务器上。然后，在 2000 年左右，那些对延迟不敏感的应用通常被部署到虚拟服务器上。对于雲端原生应用，它们被打包成 docker 镜像并部署在容器中。

4. 应用基础设施

   这些应用被大量部署在云基础设施上，而不是在自托管服务器上。

## 開發者生產力工具

### 視覺化 JSON 文件

嵌套的 JSON 文件是难以阅读的。

**JsonCrack** 根据 JSON 文件生成图表，从而使其易于阅读。

此外，生成的图表可以下载为图片。

<p>
  <img src="../images/json-cracker.jpeg" />
</p>


### 自动将代码转换为架構图

<p>
  <img src="../images/diagrams_as_code.jpeg" style="width: 640px" />
</p>


它的用处是什么？

- 通过编写 Python 代码绘制云系统架構。
- 也可以直接在 Jupyter Notebooks 中渲染图表。
- 无需设计工具。
- 支持以下提供商：AWS、Azure、GCP、Kubernetes、 Alibaba Cloud、Oracle Cloud 等等。

[Github 仓库](https://github.com/mingrammer/diagrams)

## Linux

### Linux 文件系统解析

<p>
  <img src="../images/linux-file-systems.jpg" style="width: 680px" />
</p>

过去，Linux 文件系统就像一个无组织的城镇，人们可以随心所欲地在他们喜欢的地方建造自己的房子。然而，在 1994 年的时候，文件系统层次结构标准（Filesystem Hierarchy Standard，FHS）被引入，从而为 Linux 文件系统带来了秩序。

通过实施诸如 FHS 这样的标准，软件可以确保在各种 Linux 发行版上的布局一致。尽管如此，并非所有 Linux 发行版都严格遵守此标准。它们通常会融入自己独特的元素或满足特定的要求。
要精通此标准，您可以从探索它开始。使用“cd”等指令进行导航，使用“ls”等指令列出目錄内容。将文件系统想象成一棵从根 (/) 开始的树。随着时间的推移，您将自然而然地使用它，从而使您成为熟练的 Linux 管理员。

### 你应该知道的 18 个最常用的 Linux 指令

Linux 指令是用来与操作系统交互的指令。它们帮助我们管理文件、目錄、系统进程、以及系统的许许多多其他方面的内容。为了高效地导航和维护基于 Linux 的系统，您需要熟悉这些指令。

下图显示了流行的 Linux 指令：

<p>
  <img src="../images/18 Most-Used Linux Commands You Should Know-01.jpeg" style="width: 680px" />
</p>


- ls - 列出文件和目錄
- cd - 更改当前目錄
- mkdir - 创建一个新的目錄
- rm - 删除文件或者目錄
- cp - 拷贝文件或者目錄
- mv - 移动或重命名文件或者目錄
- chmod - 更改文件或者目錄权限
- grep - 在文件中搜索指定模式的内容
- find - 搜索文件或者目錄
- tar - 操作 tarball 归档文件
- vi - 使用文本编辑器编辑文件
- cat - 显示文件内容
- top - 显示进程和资源使用情况
- ps - 显示进程信息
- kill - 通过发送信号来终止进程
- du - 评估文件空间使用情况
- ifconfig - 配置網路介面
- ping - 测试主机之间的網路连通性

## 安全

### HTTPS 是如何運作的？

超文本传输安全協定（Hypertext Transfer Protocol Secure，HTTPS）是超文本传输協定（Hypertext Transfer Protocol，HTTP）的扩展。HTTPS 使用传输层安全性（Transport Layer Security，TLS）传输加密数据。即使数据被在线劫持，劫持者得到的也只是二进制码。

<p>
  <img src="../images/https.jpg" />
</p>

数据是如何被加密解密的？

步骤 1 - 客户端（浏览器）和伺服器端建立一个 TCP 连接。

步骤 2 - 客户端发送一条“client hello”消息给伺服器端。这条消息包含了一组必要的加密演算法（密码套件）以及它支持的最新的 TLS 版本。接着，伺服器端用一条“server hello”消息进行响应，以便浏览器知道它是否支持这些演算法和 TLS 版本。

接着，伺服器端发送 SSL 憑證给客户端。憑證包含公钥、主机名、过期日期等。客户端会验证此憑證。

步骤 3 - 验证 SSL 憑證后，客户端生成一个会话密钥，然后使用公钥对其进行加密。伺服器端收到了这个加密的会话密钥后，使用私钥对其进行解密。

步骤 4 - 现在，客户端和伺服器端都持有相同的会话密钥（对称加密），因此，加密数据就可以通过安全的双向通道进行传输了。

為什麼在数据传输过程中，HTTPS 要切换到对称加密呢？有两个主要原因：

1. 安全性：非对称加密只能单向进行。这意味着，如果伺服器端尝试将加密数据发送回客户端，那么任何人都可以使用公钥解密数据。

2. 服务器资源：非对称加密增加了相当多的数学计算开销。因此，它不适用于长会话中的数据传输。

### 简明扼要解释下 Oauth 2.0。

OAuth 2.0 是一个强大且安全的框架，允许不同应用代表用户安全地彼此之间进行交互，而无需共享敏感的凭据。

<p>
  <img src="../images/oAuth2.jpg" />
</p>

OAuth 中涉及的实体包括用户、服务器和身份提供商（Identity Provider，IDP）。

OAuth 令牌（OAuth Token）能做什么？

使用 OAuth 时，你会获得一个代表你身份和权限的 OAuth 令牌。这个令牌可以执行一些重要的操作：

单点登录（Single Sign-On，SSO）：使用一个 OAuth 令牌，只要进行一次登录操作，你就可以登录到多个服务或者应用，让生活轻松安全多了。

系统间授權（Authorization Across Systems）：OAuth 令牌让你可以在各个系统之间共享你的授權或者存取权限，因此，你不需要在每处单独登录。

存取用户资料（Accessing User Profile）：拥有 OAuth 令牌的应用可以存取你允许的用户资料的特定部分内容，但不会看到所有内容。

记住，OAuth 2.0 的目标是在确保你和你的数据安全的同时，让你在不同的应用和服务之间的在线体验变得更加无缝和轻松。

### 四种最常见的身份认证机制

<p>
  <img src="../images/top4-most-used-auth.jpg" />
</p>

1. SSH 密钥：

   使用加密密钥来安全存取遠端系统和服务器。

2. OAuth 令牌：

   令牌为第三方应用提供对用户数据的有限存取权限。

3. SSL 憑證：

   數位憑證确保伺服器端和客户端之间的安全和加密通信。

4. 凭据：

   使用用户身份验证信息来验证并授予对各种系统和服务的存取权限。

### 会话、Cookie、JWT、令牌、SSO 和 OAuth 2.0 - 它们分别是什么？

这些术语都与用户身份管理相关。当你登录进一个网站时，你要声明自己是谁（身份验证，identification）。你的身份经过验证（认证,authentication），并被授予必要的权限（授權，authorization）。过去，许多解决方案被提出来，而这个解决方案列表还在不断增长中。

<p>
  <img src="../images/session.jpeg" />
</p>

由简而繁，下面是我关于用户身份管理的理解：

- WWW-Authenticate 是最基本的方法。浏览器要求你提供用户名和密码。由于无法控制登录生命周期，因此现今已经很少使用了。

- 对登录生命周期有更精细的控制的是 session-cookie。服务器维护会话存储，浏览器保留会话 ID。Cookie 通常仅适用于浏览器，不太适用于移动应用。

- 要解决相容性问题，可以使用令牌。客户端将令牌发送到服务器，然后服务器验证令牌。这种方法的缺点是需要对令牌进行加密和解密，这一过程可能会耗时。

- JWT 是表示令牌的标准方式。由于可以对这些信息进行數位簽章，因此它们可以被验证和信任。由于 JWT 包含签名，因此无需在伺服器端保存会话信息。

- 通过使用 SSO（单点登录），您只需进行一次登录操作，即可登录到多个网站。它使用CAS（central authentication service，中央认证服务）来维护跨站点信息。

- 通过使用 OAuth 2.0，你可以授權一个网站存取你在另一个网站上的信息。

### 如何将密码安全地存储到資料庫中，以及如何验证密码？

<p>
  <img src="../images/salt.jpg" style="width: 720px" />
</p>


**不要做的事**

- 明文存储密码并非明智之举，因为任何一个具有内部存取权限的人都可以看到它们。

- 直接存储密码哈希值并不够，因为它容易受到预计算攻击（precomputation attack）的影响，例如彩虹表（rainbow table）。

- 要缓解预计算攻击，我们使用 salt 来加密密码。

**什麼是 salt？**

根据 OWASP 指南，“salt 是在散列过程中新增到每个密码中的随机生成的唯一字符串”。

**如何存储密码和 salt？**

1. 哈希结果对于每个密码都是唯一的。
2. 密码可以以以下格式存储在資料庫中：hash(password + salt)。

**如何验证密码？**

要验证一个密码，可以经过以下过程：

1. 客户端输入密码。
2. 系统从資料庫中获取对应的 salt。
3. 系统将 salt 附加到密码后，然后对结果进行哈希操作。让我们将哈希过的值称为 H1。
4. 系统对比 H1 和 H2（資料庫中存储的哈希值）。如果二者相等，那么密码就是有效的。

### 向一个十岁小孩解释 JSON Web Token (JWT)

<p>
  <img src="../images/jwt.jpg" />
</p>

想象一下，你有一个特殊的盒子，叫做 JWT。这个盒子里有三个部分：一个头部、一个数据体和一个签名。

头部就像盒子外部的标签。它告诉我们盒子的类型以及如何保护它。通常以 JSON 的格式（只是一种使用花括号"{ }"和冒号“:”组织信息的方式）编写。

数据体就像你想要发送的实际消息或者信息。可以是你的名字、年龄或者任何你想要分享的数据。它也是以 JSON 格式编写的，因此，易于理解和处理。

而签名则是让 JWT 保持安全的东西。它就像一种特殊的印章，只有发送者知道如何创建它。这个签名是使用一种秘密代码生成的，有点像密码。它确保了没有人能够在发送者不知情的情况下篡改 JWT 的内容。

当你想把 JWT 发送给服务端时，你把头部、数据体和签名放进箱子里。然后把它发送到服务器。服务器可以轻松读取头部和数据体，以了解你是谁，以及你想要做什么。

### Google Authenticator（或者其它类型的两步认证器）是如何運作的？

Google Authenticator 通常用于在已启用两步验证（2-factor authentication）的情况下登录我们的账户。那么，它是如何保证安全的呢？

Google Authenticator 是一种基于软件的身份验证器，它实现了两步验证服务。下图提供了详细信息。

<p>
  <img src="../images/google_authenticate.jpeg" />
</p>


涉及两个阶段：

- 第一阶段 - 用户启用 Google 两步验证。
- 第二阶段 - 用户使用身份验证器进行登录等操作。

让我们看看这两个阶段。

**第一阶段**

步骤 1 和 2：Bob 打开网页来启用两步验证。前端请求一个密钥。身份验证服务为 Bob 生成密钥并将其存储在資料庫中。

步骤 3：身份验证服务返回一个 URI 给前端。这个 URI 由密钥颁发者、用户名和密钥组成。这个 URI以二维码的形式显示在网页上。

步骤 4：然后，Bob 使用 Google Authenticator 扫描生成的二维码。密钥存储在身份验证器中。

**第二阶段**
步骤 1 和 2：Bob 想要使用 Google 两步验证登录网站。为此，他需要密码。Google Authenticator 每30秒使用 TOTP（Time-based One Time Password，基于时间的一次性密码）演算法生成一个6位数的密码。Bob使用这个生成的密码来登录网站。

步骤 3 和 4：前端将 Bob 输入的密码发送到后端进行身份验证。身份验证服务从資料庫中读取密钥，然后使用与客户端相同的 TOTP 演算法生成一个6位数的密码。

步骤 5：身份验证服务比较客户端和服务器分别生成的两个密码，并将比较结果返回给前端。只有在两个密码匹配时，Bob 才能继续登录过程。

这种身份验证机制安全吗？

- 其他人能获取密钥吗？

  我们需要确保密钥是使用HTTPS 传输的。身份验证器客户端和資料庫存储密钥，因此，我们需要确保这些密钥是加密的。

- 黑客能猜测这个6位数密码吗？

  不能。密码有6位数字，因此，生成的密码有100万种可能的组合。此外，密码每30秒更改一次。如果黑客想要在30秒内猜测出密码，那么他们需要每秒输入30,000个组合。


## 真实案例学习

### Netflix 的技術堆疊

本文基于许多 Netflix 工程博客和开源项目的研究。若有任何不当之处，请随时告诉我们。

<p>
  <img src="../images/netflix tech stack.png" style="width: 680px" />
</p>

**移动和 Web**：Netflix 采用 Swift 和 Kotlin 来构建原生移动应用。而对于 Web 应用，它使用 React。

**前端和服务器之间的通信**：Netflix 使用 GraphQL。

**后端服务**：Netflix 依赖 ZUUL、Eureka、Spring Boot 框架和其他技术。

**資料庫**：Netflix 利用 EV Cache、Cassandra、CockroachDB 和其他資料庫。

**消息传递/流处理**：Netflix 使用 Apache Kafka 和 Fink 进行消息传递和流处理。

**视频存储**：Netflix 使用 S3 和 Open Connect 进行视频存储。

**数据处理**: Netflix 利用 Flink 和 Spark 进行数据处理，然后使用 Tableau 进行視覺化。Redshift 被用于结构化数据仓库信息的处理。

**CI/CD**：对于 CI/CD 流程，Netflix 使用各种工具，例如 JIRA、Confluence、PagerDuty、Jenkins、Gradle、Chaos Monkey、Spinnaker、Atlas 等。

### Twitter 架構 2022

是的，这就是真正的 Twitter 架構。它由 Elon Musk 发布，我们对其进行了重绘以便于更好的阅读。

<p>
  <img src="../images/twitter-arch.jpeg" />
</p>


### 过去 15 年 Airbnb 微服務架構的演进之路

Airbnb 的微服務架構经历了三个主要阶段。

<p>
  <img src="../images/airbnb_arch.jpeg" />
</p>


單體架構（Monolith） (2008 - 2017)

Airbnb 最初只是一个简单的房东房客市场。它使用 Ruby on Rails 构建 —— 單體架構。

有何挑战？

- 团队所有权混乱 + 无主代码
- 部署慢

微服務（Microservices） (2017 - 2020)

微服務旨在解决上述挑战。在微服務架構中，关键的服务包含：

- 数据获取服务
- 业务逻辑数据服务
- 写工作流服务
- UI 聚合服务
- 每一个服务都由一个团队专门负责

有何挑战？

对人类来说，数百个服务和依赖是难以管理的。

微服務 + 宏服务（Micro + macroservices） (2020 - present)

这是 Airbnb 现在正在努力实现的架構。微服務和宏服务混合模型侧重于 API 的统一。

### Monorepo vs. Microrepo.

何为最佳之选？為什麼不同的公司选择不同的选项？

<p>
  <img src="../images/monorepo-microrepo.jpg" />
</p>


Monorepo 并不是一个新东西；Linux 和 Windows 都是用 Monorepo 创建的。为了提升可伸缩性和构建速度，谷歌开发了内部专用的工具链，以便更快地对其进行扩展，并制定了严格的编码质量标准，以保持代码一致性。

Amazon 和 Netflix 是微服務理念的主要簇拥者。这种方法自然地将服务代码分开存储在不同的仓库中。它能更快地扩展，但后期可能会导致治理方面的问题。

在 Monorepo 中，每个服务都是一个文件夹，每一个文件夹都有一个 BUILD 配置和 OWNERS 权限控制。每一个服务成员负责他们自己的文件夹。

另一方面，在 Microrepo 中，每一个服务负责它们自己的仓库，而构建配置和权限通常是为整个仓库设置的。

在 Monorepo 中，无论业务是什么，整个代码库都共享依赖项，因此，当有版本升级时，每一个代码库都会升级它们的版本。

在 Microrepo 中，每一个仓库控制自己的依赖项。业务根据自己的安排选择何时升级版本。

Monorepo 有提交标准。Google 的代码评审以其高标准而闻名，确保Monorepo 具有一致的质量标准，而无论业务是什么。

Microrepo 可以设置自己的标准，也可以通过采纳最佳实践来使用共享标准。它可以更快地为业务进行扩展，但代码质量可能会有所不同。
Google 工程师构建了 Bazel，而 Meta 构建了 Buck。还可以用一些其他的开源工具，包括 Nx、Lerna 等。

多年以来，Microrepo 拥有了更多支持工具，其中包括 Java 的 Maven 和 Gradle、NodeJS 的 NPM 以及 C/C++ 的 CMake for C/C++。

### 如果是你，你要如何设计 Stack Overflow 网站？

如果你的答案是本地服务器（on-premise server）和單體架構（位于下图底部），那么你有可能面试失败，但这正是它现实中的构建方式！

<p>
  <img src="../images/stackoverflow.jpg" />
</p>


**人们觉得它应该是什么样子的呢**

面试官可能期待类似于上图顶部那样子的回答。

- 使用微服務来将系统分解为小组件。
- 每个服务都有自己的資料庫。重度使用快取。
- 服务是分片的。
- 服务之间通过消息佇列异步通信。
- 服务是使用 CQRS （Command Query Responsibility Segregation） 和 Event Sourcing 来实现的。
- 展示分散式系统方面的知识，例如最终一致性（eventual consistency）、CAP 定理等。

**实际上呢**

Stack Overflow 仅用九台本地服务器即可满足所有流量需求，而且它是單體的！它拥有自己的服务器并且并没有在云上运行。

这与我们当下所有流行的信念背道而驰。

### 為什麼 Amazon Prime Video 监控从无服务（Serverless）转向了單體架（Monolithic）？它是怎样节省九成成本的呢？

下图是迁移前后的架構对比。

<p>
  <img src="../images/serverless-to-monolithic.jpeg" />
</p>


Amazon Prime Video 监控服务是什么？

Prime Video 服务需要监控数千个直播流的质量。这个监控工具自动实时分析流，识别诸如块损坏、视频冻结和同步问题这样的质量问题。这对于提高客户满意度来说，是一个重要的过程。

共有三步：媒体转换器（media converter）、缺陷检测器（defect detector）和实时通知（real-time notification）。

- 旧架構有什么问题？

  旧架構基于 Amazon Lambda，适用于快速构建服务。然而，当大规模运行此架構时，就成本而言，并不划算。其中两个最贵的操作是：

1. 编排工作流 —— AWS Step Functions 按状态转换收费，而编排每秒会执行多次状态转换。

2. 在分散式组件之间传递数据 —— 中间数据存储在 Amazon S3 中，以便下一个阶段可以下载。当数据量很大的时候，下载操作可能很昂贵。

- 單體架構节约了九成成本

  單體架構旨在解决成本问题。在此架構中，仍然有 3 个组件，但是，媒体转换器和缺陷检测器部署在同一进程中，从而节省了通过網路传递数据所带来的开销。令人惊讶的是，这种部署架構的变更节省了九成成本！

这是一个有趣且独一无二的案例研究，因为微服務已经成为了科技行业的时尚首选。很高兴看到我们对架構的演变进行了更多的讨论，并且对其利弊也进行了更加诚实的讨论。将组件分解为分散式微服務是有成本的。

- Amazon 的领导人对此有何评论？

  Amazon 的 CTO Werner Vogel：“构建**可进化的软件系统**是一种策略，而不是一种宗教。以开放的心态审视你的架構是必须的。”

前 Amazon 可持续性副总裁 Adrian Cockcroft：“Prime Video 团队走的是我称之为**无服务优先（Serverless First）**的道路…我并不主张**仅无服务（Serverless Only）**”。

### Disney Hotstar 是如何在锦标赛期间捕获 50 亿个表情符号的？

<p>
  <img src="../images/hotstar_emojis.jpeg" style="width: 720px" />
</p>


1. 客户端通过标准的 HTTP 请求发送表情符号。你可以将 Golang 服务看成一个典型的 Web 服务器。选择 Golang 是因为它很好的支持了并发。线程在 Golang 中是轻量的。

2. 由于写入量非常大，Kafka（消息佇列）被用作缓冲区。

3. 表情符号数据由一个名为 Spark 的流处理服务来进行聚合。它每 2 秒聚合一次数据，这个时间是可配置的。根据时间间隔需要进行权衡。较短的间隔意味着，表情符号将更快地被传递给其他客户端，但同时也意味着需要更多的计算资源。

4. 将被聚合的数据写入到另一个 Kafka。

5. PubSub 消费者从 Kafka 拉取聚合的表情符号数据。

6. 通过 PubSub 基础设施，表情符号被实时传递给其他客户端。PubSub 基础设施很有意思。Hotstar 考虑了以下協定：Socketio、NATS、MQTT 和 gRPC，最终选择了 MQTT。

LinkedIn 也采用了类似的设计，每秒流式传输一百万个赞。

### Discord 是怎样存储数万亿条消息的

下图显示了 Discord 的消息存储的演进之路：

<p>
  <img src="../images/discord-store-messages.jpg" />
</p>


MongoDB ➡️ Cassandra ➡️ ScyllaDB

在 2015 年，Discord 的第一个版本建立在单个 MongoDB 副本之上。到了2015 年 11 月左右，MongoDB 已经存储了 1 亿条数据，此时，RAM 再也无法容纳数据和索引了。延迟变得不可预测。消息存储需要移到另一个資料庫。Cassandra 被选中。

在 2017 年，Discord 拥有 12 个 Cassandra 节点，存储了数十亿条消息。

到了 2022 年初，它拥有 177 个节点，存储了数万亿条消息。此时，延迟再次不可预测，而维护操作也成本过高以致无法进行。

这个问题的出现有几个原因：

- Cassandra 的内部資料結構使用了 LSM 树。读取比写入更昂贵。在具有数百用户的服务器上可能会有许多并发读取操作，从而导致热点问题。
- 维护集群，例如紧凑的 SSTable，这会影响性能。
- 垃圾回收暂停会导致显著的延迟波动

ScyllaDB 是一种相容 Cassandra 的資料庫，用C++编写。Discord 重新设计了其架構，使其具有一个單體 API，一个用 Rust 编写的数据服务以及基于 ScyllaDB 的存储。

ScyllaDB 中的 p99 读取延迟为15 毫秒，而 Cassandra 则为 40-125 毫秒。p99 写入延迟为 5 毫秒，而 Cassandra 则为 5-70 毫秒。

### YouTube、TikTok Live 或 Twitch 上的视频直播是如何運作的呢？

直播与常规的流媒体不同，因为直播的视频内容是通过互联网实时传输的，通常延迟只有几秒钟。

下图解释了使其成为可能的幕后工作流。

<p>
  <img src="../images/live_streaming_updated.jpg" style="width: 640px" />
</p>


步骤 1：麦克风和摄像头捕获原始视频数据。数据稍后被发送到伺服器端。

步骤 2：视频数据被壓縮和编码。例如，壓縮演算法将背景与其他视频元素分离。壓縮后，视频被编码为诸如 H.264 之类的标准。在此步骤之后，视频数据的大小会小得多。

步骤 3：编码数据被分成更小的段，每一段长度通常为几秒，因此，大大缩短了下载或者流式传输的时间。

步骤 4：发送分段数据到流媒体服务器。流媒体服务器需要支持不同的裝置和網路条件。这称为“自适应比特率流式传输（Adaptive Bitrate Streaming）”。这意味着我们在步骤2和步骤3中需要生成具有不同比特率的多个文件。

步骤 5：推送直播流数据到由 CDN（Content Delivery Network，内容传输網路）支持的边缘服务器（edge server）。数百万观众可以从附近的边缘服务器观看视频。CDN 显著降低了数据传输延迟。

步骤 6：观众的裝置解码和解压视频数据，并在视频播放器中播放视频。

步骤 7 和 8：如果需要存储视频以供重播，那么编码数据会被发送到存储服务器（storage server），观众可以稍后从中请求重播。

直播流媒体的标准協定包括：

- RTMP（Real-Time Messaging Protocol，实时消息传输協定）：该協定最初由 Macromedia 开发，用于在 Flash 播放器和服务器之间传输数据。现在，它用来通过互联网传输视频数据。注意，视频会议應用程式（如Skype）使用 RTC（Real-Time Communication，实时通信）協定来获得更低的延迟。
- HLS（HTTP Live Streaming，HTTP实时流传输）：它要求 H.264 或 H.265 编码。Apple 裝置仅接受 HLS 格式。
- DASH（Dynamic Adaptive Streaming over HTTP，基于HTTP的动态自适应流传输）：DASH不支持Apple裝置。
- HLS 和 DASH 都支持自适应比特率流传输。

## 许可

<p xmlns:cc="http://creativecommons.org/ns#" >This work is licensed under <a href="http://creativecommons.org/licenses/by-nc-nd/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC-ND 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nd.svg?ref=chooser-v1"></a></p>

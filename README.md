#Data Coolection and Persistence
利用Elasticsearch, logstash蒐集Twitter社群推文內容並儲存
***
##資料格式 ( JSON Format )
###資料欄位
+ created_at - 發表推文時間
+ text -  推文內容
+ source - 推文來源網址
+ user - 推文者資訊
	+ id - 使用id
	+ name - 使用名稱
	+ location - 位置
	+ followers_count - 追隨者人數
	+ friends_count - 好友人數
	+ favourites - 設定為最愛數量
	+ time_zone - 所在時區
	+ geo_enabled - 定位開啟與否
	+ lang - 語言
+  retweeted_status- 推文回應資訊
	+ created_at - 發表推文時間
	+ text -  推文內容
	+ source - 推文來源網址
	+ user - 推文者資訊
		+ id - 使用id
		+ name - 使用名稱
		+ location - 位置
		+ followers_count - 追隨者人數
		+ friends_count - 好友人數
		+ favourites - 設定為最愛數量
		+ time_zone - 所在時區
		+ geo_enabled - 定位開啟與否
		+ lang - 語言

##資料來源 ( Data Sources )
### (1) API 來源：
Twitter API  [The Link][1] 
[1]: https://dev.twitter.com/overview/documentation/ "Developer Web Site of Twitter"

### (2) 內容主題：
搜尋Twitter推文有關美國總統候選人-川普【Trump】相關的推文討論

### (3) 查詢字串：
查詢字串：Trump

##程式碼連結
+ 使用logstash抓取twitter資料並儲存於Elasticsearch [[view code]][2]

[2]: https://github.com/Jeng-Feng/BigDataAnalysis/blob/master/crawler/twitter2elasticsearch-conf  "view code for twitter2elasticsearch-conf"
+ 透過logstash讀取Elasticsearch資料輸出到文字檔案 (預設json格式) [[view code]][3]
[3]: https://github.com/Jeng-Feng/BigDataAnalysis/blob/master/crawler/elasticsearch2Json-conf "view code for elasticsearch2Json-conf"
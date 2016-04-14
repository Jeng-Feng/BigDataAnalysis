#Homework 1：Data Coolection and Persistence
##資料格式 ( JSON Format )
###資料欄位
+ Red
+ Green
+ 
##資料來源 ( Data Sources )
### (1) API 來源：
### (2) 內容主題：
### (3) 查詢字串：

1. read
2. re1
3. redd
##程式碼連結
+ twitter資料抓取並轉入Elasticsearch [twitter2elasticsearch-conf][1]

[1]: http://google.com/  "twitter2elasticsearch-conf"

<pre><code>
input{
	twitter {
	    consumer_key => "Xp7MuJeniplsKSm01ZHAvlTqx"
	    consumer_secret => "ag9rU1AxorluvTyXc4kz2I56S1K4lZyZdOFUjMBrpkBfetdOVo"
	    oauth_token => "279775375-tVXzqsKpVO6y030btX0UU0UXHlSBwU3ZA4hm8M8Z"
	    oauth_token_secret => "gdw1fLAg7RSEN0e0sahHhwsV8rXOBdOoaMRIqFdoElcr7"
	    keywords => ["Trump"]
	    full_tweet => true
	}
}
output{
		elasticsearch{
                    index => "twitter"
        }
}
</core></pre>

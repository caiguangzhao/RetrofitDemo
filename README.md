# RetrofitDemo

基于Retrofit 2.1.0网络请求框架，请求天气数据。项目采用MVP架构。

* 天气API接口：聚合数据

* API接口返回的json数据格式
```
{
	"reason":"successed!",

	"result":{
		"data":{
			"realtime":{
				"wind":{"windspeed":"7.0","direct":"南风","power":"1级","offset":null},
				"time":"15:00:00",
				"weather":{"humidity":"66","img":"1","info":"多云","temperature":"31"},
				"dataUptime":1470902400,
				"date":"2016-08-11",
				"city_code":"101280101",
				"city_name":"广州",
				"week":4,
				"moon":"七月初九"
				},
			"life":{
				"date":"2016-8-11",
				"info":{
					"kongtiao":["部分时间开启","天气热，到中午的时候您将会感到有点热，因此建议在午后较热时开启制冷空调。"],
					"yundong":["较不宜","有降水，推荐您在室内进行健身休闲运动；若坚持户外运动，须注意携带雨具并注意避雨防滑。"],
					"ziwaixian":["中等","属中等强度紫外线辐射天气，外出时建议涂擦SPF高于15、PA+的防晒护肤品，戴帽子、太阳镜。"],
					"ganmao":["少发","各项气象条件适宜，发生感冒机率较低。但请避免长期处于空调房间中，以防感冒。"],
					"xiche":["不宜","不宜洗车，未来24小时内有雨，如果在此期间洗车，雨水和路上的泥水可能会再次弄脏您的爱车。"],
					"wuran":["良","气象条件有利于空气污染物稀释、扩散和清除，可在室外正常活动。"],
					"chuanyi":["热","天气热，建议着短裙、短裤、短薄外套、T恤等夏季服装。"]}
				},
			"weather":[
				{
					"date":"2016-08-11",
				 	"info":{
					 	"night":["4","雷阵雨","26","无持续风向","微风","19:02"],
						"day":["4","雷阵雨","32","无持续风向","微风","06:01"]},
				 	"week":"四","nongli":"七月初九"
				},
				{
					"date":"2016-08-12",
				 	"info":{
				 		"dawn":["4","雷阵雨","26","无持续风向","微风","19:02"],
				 		"night":["9","大雨","26","无持续风向","微风","19:01"],
				 		"day":["9","大雨","31","无持续风向","微风","06:02"]},
				 	"week":"五",
				 	"nongli":"七月初十"
				 },
				 {
				 	"date":"2016-08-13",
				 	"info":{
				 		"dawn":["9","大雨","26","无持续风向","微风","19:01"],
				 		"night":["4","雷阵雨","25","无持续风向","微风","19:00"],
				 		"day":["4","雷阵雨","31","无持续风向","微风","06:02"]},
				 	"week":"六","nongli":"七月十一"
				 },
				 {
				 	"date":"2016-08-14",
				 	"info":{
				 		"dawn":["4","雷阵雨","25","无持续风向","微风","19:00"],
				 		"night":["22","中雨-大雨","26","无持续风向","微风","19:00"],
				 		"day":["4","雷阵雨","32","无持续风向","微风","06:02"]},
				 	"week":"日","nongli":"七月十二"
				 },
				 {
				 	"date":"2016-08-15",
				 	"info":{
				 		"dawn":["22","中雨-大雨","26","无持续风向","微风","19:00"],
				 		"night":["9","大雨","26","北风","3-4 级","18:59"],
				 		"day":["22","中雨-大雨","32","无持续风向","微风","06:03"]},
				 	"week":"一","nongli":"七月十三"
				 },
				 {
				 	"date":"2016-08-16",
				 	"info":{
				 		"night":["1","多云","26","","微风","19:30"],
				 		"day":["4","雷阵雨","32","","微风","07:30"]},
				 	"week":"二","nongli":"七月十四"
				 },
				 {
				 	"date":"2016-08-17",
				 	"info":{
				 		"night":["0","晴","26","东北风","微风","19:30"],
				 		"day":["4","雷阵雨","33","东北风","微风","07:30"]},
				 	"week":"三","nongli":"七月十五"
				 }],

			"pm25":{
				"key":"",
				"show_desc":0,
				"pm25":{"curPm":"38","pm25":"21","pm10":"38","level":1,"quality":"优","des":"今天的空气质量令人满意，各类人群可正常活动。"},
				"dateTime":"2016年08月11日16时","cityName":"广州"},

			"date":null,"isForeign":0
		}
	},
	
	"error_code":0
}
```

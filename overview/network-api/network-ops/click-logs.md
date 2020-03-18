# Click Logs

| HTTP Method | End Point |
| :--- | :--- |
| GET | /network/clicks |

## Request Parameters

| Key | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| start | String | Start Date in YYYY-MM-DD format | yes |
| end | String | End Date in YYYY-MM-DD format | yes |
| campaign\_id | Array\[\] of String or Integer | Array of campaign Ids, eg: It can be `Integer` or `String` \(24 char\) | yes |
| publisher\_id | Array\[\] of String or Integer | Array of affiliate Ids eg: Id can be `Integer` or `String` \(24 char\) | yes |
| fields | Array\[\] of String | fields that are to be displayed | yes |
| limit | Integer | How many record you want in response. By default is consider `1000` and  Maximum value is `1000` | yes |
| page | Intege | Page Number | yes |

```text
?apiKey={API_KEY_HERE}&start={YYYY-MM-DD}&end={YYYY-MM-DD}&campaign_id[]={campaign_id}&limit=10&page=1
```

_Remember whatever params you send in query will be visible under the **response.query** object_

## Response body

```bash
curl -H 'X-Api-Key: {key}' -X GET 'http://api.trackier.com/network/clicks?apiKey={API_KEY_HERE}&start={YYYY-MM-DD}&end={YYYY-MM-DD}&campaign_id[]={campaign_id}&limit=10&page=1'
```

```javascript
{
   "success":true,
   "data":{
      "clicks":[
         {
            "p1":"",
            "ipaddr":"107.178.192.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:18:58",
            "_id":"5c878e9a802fbe04973e8f3e",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.194.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:17:58",
            "_id":"5c878e5ec404ab046d6ad5b3",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.192.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:16:58",
            "_id":"5c878e22802fbe04973e2023",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.194.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:16:00",
            "_id":"5c878de8c404ab046d6a67af",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.192.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:14:58",
            "_id":"5c878daa802fbe04973db8d6",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.194.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:13:59",
            "_id":"5c878d6fc404ab046d6a0184",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.192.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:12:56",
            "_id":"5c878d30c404ab046d69ccaa",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.195.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:11:59",
            "_id":"5c878cf7c404ab046d69996d",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.192.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:10:57",
            "_id":"5c878cb9802fbe04973ce80b",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         },
         {
            "p1":"",
            "ipaddr":"107.178.192.0",
            "country":"US",
            "device":"unknown",
            "browser":"Unknown",
            "created":"2019-03-12 16:09:58",
            "_id":"5c878c7e802fbe04973cb98c",
            "campaign_id":16,
            "campaign_long_id":"58551c30b6920d760817f711",
            "campaign_title":"Traffic Arbitrage Book",
            "publisher_id":31,
            "publisher_long_id":"59a54a6b89d4465afb339a32",
            "publisher_name":"vNative Account",
            "lp":"Test URL",
            "lp_id":1,
            "lp_long_id":"5a095cf4b6920d156e780efa",
            "sl":""
         }
      ],
      "fieldMap":{
         "_id":"Click ID",
         "source":"Source",
         "ipaddr":"IP Address",
         "ua":"User Agent",
         "cookie":"Cookie",
         "os":"Operating System (OS)",
         "city":"City",
         "isp":"Carrier (ISP)",
         "p1":"P1",
         "p2":"P2",
         "p3":"P3",
         "p4":"P4",
         "p5":"P5",
         "p6":"P6",
         "p7":"P7",
         "p8":"P8",
         "p9":"P9",
         "p10":"P10",
         "note":"Note",
         "gaid":"GAID",
         "idfa":"IDFA",
         "app_id":"App ID",
         "app_name":"App Name",
         "aid":"Android ID",
         "cr_name":"Creative Name",
         "sl":"Smart Link",
         "payout":"Payout",
         "revenue":"Revenue",
         "country":"Country",
         "browser":"Browser",
         "referer":"Referrer",
         "device":"Device",
         "created":"Created",
         "campaign_id":"Campaign ID",
         "campaign_long_id":"Campaign Long ID",
         "campaign_title":"Campaign Title",
         "publisher_id":"Publisher ID",
         "publisher_long_id":"Publisher Long ID",
         "publisher_name":"Publisher Name",
         "lp":"Landing Page",
         "lp_id":"Landing Page ID",
         "lp_long_id":"Landing Page Long ID"
      },
      "query":{
         "start":"2019-03-12",
         "end":"2019-03-12",
         "campaign_id":[
            "16"
         ],
         "publisher_id":[

         ],
         "fields":[
            "_id",
            "p1",
            "ipaddr",
            "campaign_id",
            "publisher_id",
            "country",
            "device",
            "browser",
            "created"
         ]
      },
      "pagination":{
         "per_page":10,
         "current_page":1,
         "total":979
      }
   }
}
```


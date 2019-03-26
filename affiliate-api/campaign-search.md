# Campaign Search

| **HTTP method** | **End Point** | **Description** |
| :--- | :--- | :--- |
| GET | /affiliate/campaign-search | Search Campaigns |

This Endpoint searches all the campaigns allotted to publisher whose preview url domain matches the domain of the deeplink given in param **p4**

## **Sample Request**

```bash
curl -i -X GET -H "X-Api-Key: {key}" 
 'https://api.vnative.com/affiliate/campaign-search?p1=256ef263-5b50-d2d8-ca1b-093569a2e36d&p2=&p3=&p4=http%3A%2F%2Fwww.fakingnews.firstpost.com%2Fbuzzpoop%2F7-facts-gst-know-21784'
```

### **Response body**

```json
{
	"success": true,
	"data": {
		"campaigns": [
			{
				"_id": "id",
				"display_id": 43,
				"title": "Campaign Title",
				"preview_url": "http://www.fakingnews.firstpost.com/politics/shiv-sena-mp-ravindra-gaikwad-buys-hot-air-balloon-20276",
				"tracking_link": {
					"url": "http://trk.vnative.com/58edd6aab6920d574836bd52?p1=256ef263-5b50-d2d8-ca1b-093569a2e36d&p2=&p3=",
					"live": true
				},
				"permission": {
					"hasPermission": false,
					"permRequired": false,
					"access": {
						"_id": null,
						"live": false
					}
				}
			},
			{
				"_id": "od",
				"display_id": 56,
				"title": "Campaign Title",
				"preview_url": "http://www.fakingnews.firstpost.com/sponsored/person-forgot-fathers-day-every-year-finally-remembers-due-india-pak-match-takes-selfie-dad-21530",
				"tracking_link": {
					"url": "http://sd.vnative.net/5944064d17c452225d104174?p1=256ef263-5b50-d2d8-ca1b-093569a2e36d&p2=&p3=",
					"live": true
				},
				"permission": {
					"hasPermission": false,
					"permRequired": false,
					"access": {
						"_id": null,
						"live": false
					}
				}
			},
			{
				"_id": "id",
				"display_id": 77,
				"title": "Campaign Title",
				"preview_url": "http://www.fakingnews.firstpost.com/sponsored/man-searching-best-priced-smartphone-girlfriend-spends-much-time-retail-stores-ends-losing-girlfriend-22261",
				"tracking_link": {
					"url": "http://sa.vnative.net/59e30dc6b6920d48866d93fc?p1=256ef263-5b50-d2d8-ca1b-093569a2e36d&p2=&p3=",
					"live": true
				},
				"permission": {
					"hasPermission": false,
					"permRequired": false,
					"access": {
						"_id": null,
						"live": false
					}
				}
			},
			{
				"_id": "id",
				"display_id": 90,
				"title": "Campaign Title",
				"preview_url": "http://www.fakingnews.firstpost.com/buzzpoop/celebrities-celebrated-teacher-23058",
				"tracking_link": {
					"url": "http://ss.vnt.com/59ec4b54b6920d42f354f8b4?p1=256ef263-5b50-d2d8-ca1b-093569a2e36d&p2=&p3=",
					"live": true
				},
				"permission": {
					"hasPermission": false,
					"permRequired": false,
					"access": {
						"_id": null,
						"live": false
					}
				}
			},
			{
				"_id": "id",
				"display_id": 95,
				"title": "Campaign Title",
				"preview_url": "http://www.fakingnews.firstpost.com/social-media/instagram-due-maintenance-food-bloggers-lose-employment-23899",
				"tracking_link": {
					"url": "http://trk.vnative.com/59f8cd2889d4466ebe3337e2?p1=256ef263-5b50-d2d8-ca1b-093569a2e36d&p2=&p3=",
					"live": true
				},
				"permission": {
					"hasPermission": false,
					"permRequired": false,
					"access": {
						"_id": null,
						"live": false
					}
				}
			}
		],
		"pagination": {
			"page": 1,
			"totalPages": 1
		}
	}
}
```




---
title: Remixjobs API Docs


toc_footers:
  - <a href='http://remixjobs.com'>Remixjobs</a>


search: true
---

# Introduction

Welcome to the Remixjobs API!

 You can use our API to access Remixjobs API endpoints.

# Authentication

When getting api you should use an access token assigned to a user you want to act as. Access token cat be put to a bearer header or used in a get param.


# Advantages

Operations on Company Advantages

## Get All Advantages

Retrieve information about all companies advantages using the following URL:

### HTTP Request

`GET http:/remixjobs.com/api/advantages.{_format}`

> The above command returns JSON structured like this:

```json
{"advantages":[{"id":1,"name":"Baby foot"},{"id":2,"name":"Ticket restaurant"},{"id":3,"name":"Comit\u00e9 Entreprise"},{"id":4,"name":"Horaires flexibles"},{"id":5,"name":"Mutuelle sant\u00e9"},{"id":6,"name":"Cong\u00e9s pay\u00e9s suppl\u00e9mentaires"},{"id":7,"name":"Plan de retraitre compl\u00e9mentaire"},{"id":8,"name":"Cheque Emploi Service Universel (CESU)"},{"id":9,"name":"Participation"},{"id":10,"name":"Int\u00e9ressement"},{"id":11,"name":"Plan Epargne Entreprise (CEE)"},{"id":12,"name":"Ch\u00e8que Vacances"}]}
```

This endpoint retrieves all advantages.

### HTTP Return Codes

Code | Meaning
---------- | -------
200 |Returned when successful
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- Returned when user is not employer

## Retrieve an Advantage details.

Get some more information about a selected Advantage

### HTTP Request

`GET http:/remixjobs.com/api/advantages/{advantageId}.{_format}`

> The above command returns JSON structured like this:

```json
{"advantage":{"id":1,"name":"Baby foot"}}
```

This endpoint retrieves some more information about a selected Advantage/

### Query Parameters

Parameter | Description
advantageId | The ID of the Advantage to retrieve

### HTTP Return Codes

Code | Meaning
---------- | -------
200 |Returned when successful
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- Returned when user is not employer
404 | Not Found -- Returned when advantage is not found

## Update an Advantage

Updates the selected advantage information

<aside class="notice">This action is available for admin only</aside>

### HTTP Request

`PUT http:/remixjobs.com/api/advantages/{advantageId}.{_format}`

> The above command returns JSON structured like this:

```json
{"advantage":{"id":1,"name":"Baby foot"}}
```

### Query Parameters

Parameter | Description
advantageId | The ID of the Advantage to update

### HTTP Return Codes

Code | Meaning
---------- | -------
200 |Returned when successful
400 | Bad Request -- Returned when invalid data has sent
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- Returned when user is not admin
404 | Not Found -- Returned when advantage is not found

## Delete an Advantage

Deletes the selected advantage

<aside class="notice">This action is available for admin only</aside>

### HTTP Request

`DELETE http:/remixjobs.com/api/advantages/{advantageId}.{_format}`

### Query Parameters

Parameter | Description
advantageId | The ID of the Advantage to delete

### HTTP Return Codes

Code | Meaning
---------- | -------
204 |Returned when successful
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- Returned when user is not admin
404 | Not Found -- Returned when advantage is not found

# Employers

Operations on Employers

## Get a list of Employers

Gets a list of Employers (Companies) with images and other required informations.

### HTTP Request

`GET http:/remixjobs.com/api/employers.{_format}`

> The above command returns JSON structured like this:

```json
{"employers":[{"id":"e1","employer":1,"name":"foo company","email":"e-1-dummy@remixjobs.com","picture":null,"website":"http:\/\/www.example.com\/e-1","year_create":null,"location":null,"address":"135 Corwin Roads Suite 202","zipcode":"21720-3644","city":"New Justen","country_code":"FR","country":"France","vat":null,"description":"foo comapny description","is_recruiting":true,"type":0,"company_average_age":null,"twitter":"remixjobs_dev","developer_count":0,"jobs_count":14,"company_name":"foo company","company_logo":null,"company_website":"http:\/\/www.example.com\/e-1","company_year_create":null,"company_location":null,"company_address":"135 Corwin Roads Suite 202","company_description":"foo comapny description","company_city":"New Justen","company_count_employees":82,"company_page":[],"company_visible":false,"logo":null,"phone":"123-321","_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/company\/foo-company\/1\/recrutement-web"}},"technologies":[{"id":1,"name":"PHP","logo_url":null,"category":"ENVIRONMENT"},{"id":2,"name":"Symfony","logo_url":null,"category":"LANGUAGE"}],"advantages":[{"name":"Ticket restaurant"},{"name":"Horaires flexibles"},{"name":"Mutuelle sant\u00e9"}],"pictures":[{"url":"http:\/\/dev.remixjobs.com\/media\/cache\/resolve\/1600x1200_thumbnail\/1442318126-857f8b238f4988a20ffcd418dddba942.png","position":0},{"url":"http:\/\/dev.remixjobs.com\/media\/cache\/resolve\/1600x1200_thumbnail\/1442318126-efd20485958464c5ee323091c28b70c2.png","position":0}],"jobs":[{"id":1,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":["suscipit","voluptatem"],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/1"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/1"}}},{"id":5,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/11"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/5"}}},{"id":9,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/21"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/9"}}},{"id":13,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/31"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/13"}}},{"id":17,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/41"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/17"}}},{"id":21,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/51"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/21"}}},{"id":25,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/61"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/25"}}},{"id":29,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/71"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/29"}}},{"id":33,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/81"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/33"}}},{"id":37,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/91"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/37"}}},{"id":41,"title":"stagiaire webdesign et int\u00e9gration","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":3,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/101"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/stagiaire-webdesign-et-integration\/41"}}},{"id":46,"title":"Test job 1","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":2,"paycheck_period":"YEARLY","listTitle":"Full Stack Web Developer","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"marketing","localized_name":"Marketing","localized_menu_name":"Marketing","rss":"http:\/\/feeds.feedburner.com\/RJmarketing","feedburner_id":"RJmarketing","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/1"},"geolocation":{"short_formatted_address":"Lyon\u00a0(69)","formatted_address":"Lyon, France","lat":45.767299,"lng":4.8343287},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Marketing\/Test-job-1\/46"}}},{"id":47,"title":"Test job 2","contract_type":"CDI","description":"Ce poste s'adresse \u00e0 des profils junior\/d\u00e9butants - H\/F uniquement","paycheck":5,"paycheck_period":"YEARLY","listTitle":"Ergonomie","experience":"","study":"FIVE","company_website":"http:\/\/www.unikity.fr","company_name":"Unikity","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":true,"categories":[{"name":"design","localized_name":"Design","localized_menu_name":"Design","rss":"http:\/\/feeds.feedburner.com\/RJdesign","feedburner_id":"RJdesign","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/1"},"geolocation":null,"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Design\/Test-job-2\/47"}}},{"id":49,"title":"Business Development Manager H F","contract_type":"CDD","description":"Exp\u00e9riences et comp\u00e9tences requises\n\n* Vous poss\u00e9dez une formation orient\u00e9e commerce \/ marketing \/ communication\n* Vous \u00eates organis\u00e9(e), rigoureux(se), dynamique, d\u00e9brouillard(e) et poss\u00e9dez imp\u00e9rativement de r\u00e9elles qualit\u00e9s r\u00e9dactionnelles, ainsi que relationnelles\n* Vous aimez vous int\u00e9grer au sein d\u2019une \u00e9quipe ambitieuse\n* Vous poss\u00e9dez une certaine culture du web\n","paycheck":7,"paycheck_period":"YEARLY","listTitle":"Commercial \/ Business Developer","experience":"","study":"FIVE","company_website":"http:\/\/www.orange.fr","company_name":"Orange","company_logo":null,"tags":[],"status":"VALIDATED","soldout":false,"validation_time":"2011-04-26T17:26:04+0300","creation_time":"2010-02-08T13:57:05+0200","telecommute":false,"categories":[{"name":"network","localized_name":"R\u00e9seau","localized_menu_name":"R\u00e9seau","rss":"http:\/\/feeds.feedburner.com\/RJreseau","feedburner_id":"RJreseau","twitter_url":"https:\/\/twitter.com\/RemixjobsCatDev","twitter_screen_name":"RemixjobsCatDev"}],"short_url":{"short_url":"http:\/\/dev.rj.am\/101"},"geolocation":{"short_formatted_address":"Paris\u00a0(75)","formatted_address":"Paris, France","lat":48.8566667,"lng":2.3509871},"highlight":false,"address":null,"city":null,"company":null,"_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/emploi\/Reseau\/Business-Development-Manager-H-F\/49"}}}],"job_titles":["stagiaire webdesign et int\u00e9gration","Test job 1","Test job 2","Business Development Manager H F"],"contract_types":["CDI","CDD"],"job_categories":["design","marketing","network"]},{"id":"e2","employer":1,"name":"foo company","email":"e-2-dummy@remixjobs.com","picture":"http:\/\/dev.remixjobs.com\/media\/cache\/resolve\/1600x1200_thumbnail\/1442318126-857f8b238f4988a20ffcd418dddba942.png","website":"http:\/\/www.example.com\/2","year_create":null,"location":null,"address":"135 Corwin Roads Suite 202","zipcode":"21720-3644","city":"New Justen","country_code":"FR","country":"France","vat":null,"description":"foo comapny description","is_recruiting":false,"type":0,"company_average_age":null,"twitter":null,"developer_count":0,"jobs_count":0,"company_name":"foo company","company_logo":"http:\/\/dev.remixjobs.com\/media\/cache\/resolve\/1600x1200_thumbnail\/1442318126-857f8b238f4988a20ffcd418dddba942.png","company_website":"http:\/\/www.example.com\/2","company_year_create":null,"company_location":null,"company_address":"135 Corwin Roads Suite 202","company_description":"foo comapny description","company_city":"New Justen","company_count_employees":82,"company_page":[],"company_visible":false,"logo":{"url":"http:\/\/dev.remixjobs.com\/media\/cache\/resolve\/1600x1200_thumbnail\/1442318126-857f8b238f4988a20ffcd418dddba942.png","path":"\/dev\/upload\/pics\/1442318126-857f8b238f4988a20ffcd418dddba942.png"},"phone":"123-321","_links":{"www":{"href":"http:\/\/dev.remixjobs.com\/company\/foo-company\/2\/recrutement-web"}},"technologies":[{"id":1,"name":"PHP","logo_url":null,"category":"ENVIRONMENT"}],"advantages":[{"name":"Comit\u00e9 Entreprise"}],"pictures":[{"url":"http:\/\/dev.remixjobs.com\/media\/cache\/resolve\/1600x1200_thumbnail\/1442318126-dfbc3a0f7ec015130335a7a4798d22b6.png","position":0},{"url":"http:\/\/dev.remixjobs.com\/media\/cache\/resolve\/1600x1200_thumbnail\/1442318126-857f8b238f4988a20ffcd418dddba942.png","position":0}],"jobs":[],"job_titles":[],"contract_types":[],"job_categories":[]}]}
```

### Query Parameters

Parameter | Default | Description | Parameter Type | Data Type
--------- | ------- | ----------- | ----------- | -----------
limit | Set up in Config | Min 1, max 100 | query | integer
page | 1 | ~ | query | integer
complete_profile |  | If set it returns only companies with complete profile. | query | integer
popular |  | If set it returns only popular companies. |	query |	integer
hired |  |  If set it returns only companies with non-soldout jobs. |	query |	integer
period | | If set it returns only companies published in last x weeks. |	query |	integer
order | | Define an order of results. Now only popularity and number of applications supports |	query |	string

<aside class="success">
Works without authorization (i.e. an access token is not required)
</aside>

### HTTP Return Codes

Code | Meaning
---------- | -------
200 | Returned when successful


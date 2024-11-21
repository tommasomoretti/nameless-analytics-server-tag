![Na logo beta](https://github.com/tommasomoretti/nameless-analytics/assets/29273232/7d4ded5e-4b79-46a2-b089-03997724fd10)

The Nameless Analytics Server-side Client Tag is a highly customizable GTM custom template designed to claim and enhance requests from the [Nameless Analytics Client-side tracker tag](https://github.com/tommasomoretti/nameless-analytics-server-tag).

Start from here:
- [Client-side tracker tag UI](#tag-ui)
- [Basic settings](#basic-settings)
  - [Allowed domains](#allowed-domains)
  - [Endpoint path](#endpoint-path)
 


- [Event data](#event-data)
  - [Event name](#event-type)
  - [Event parameters](#event-parameters)
- [Advanced settings](#advanced-settings)
  - [Disable logs in JavaScript console for this event](#Disable-logs-in-javascript-console-for-this-event)



## Tag UI
This is the UI of the Client-side Tracker Tag.

<img width="1265" alt="Nameless Analytics server-side UI" src="https://github.com/user-attachments/assets/871e9849-e57c-4863-bc2d-437fb0549fe4">


## Basic settings
### Allowed domains
Lorem ipsum


### Endpoint path
Lorem ipsum



## Google BigQuery settings
### Project ID
Lorem ipsum


### Dataser ID
Lorem ipsum


### Table ID
Lorem ipsum


### Event parameters
#### Add/override event parameters
Lorem ipsum

#### Remove parameters manually
Lorem ipsum



## Advanced settings
### Change user cookie name
Lorem ipsum


### Change session cookie name
Lorem ipsum


### Change default session duration
Lorem ipsum


### Enable logs in debug view 
Lorem ipsum


## Cookies
When the server-side Google Tag Manager Client Tag receives the request, it checks if any cookies in there.

- If no cookies are present or the ```nameless_analytics_user``` cookie is not set but ```nameless_analytics_session cookie``` is set, the client tag generates generates two values, one for ```nameless_analytics_user``` cookie and one for ```nameless_analytics_session``` cookie), adds these values as event parameters and sets two cookies with the response.

- If the ```nameless_analytics_user``` cookie is set but ```nameless_analytics_session cookie``` is not (session expires), the client tag generates generates only one value for ```nameless_analytics_session``` cookie, adds that value to the hit, as event parameters, set again the same ```nameless_analytics_user``` cookie and set the ```nameless_analytics_session``` cookie with the response.

- If both cookies are present, the tag does not create any new cookies but adds their values to the hit.

#### Standard cookie values
| Cookie name                | Example value                                   | Default expiration | Description                                                                                     |
|----------------------------|-------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------|
| nameless_analytics_user    | pLQQFjUv7IBJuDA                                 | 400 days           | 15 chars random string                                                                          |
| nameless_analytics_session | pLQQFjUv7IBJuDA_BxEtSZuKR71XL7K-fEErCpUjYPgbVqd | 30 minutes         | nameless_analytics_user + 15 chars random string + current page_id                              |

After that, the hit will be logged in a BigQuery event date partitioned table.

<img width="1512" alt="Nameless Analytics server-side logs" src="https://github.com/user-attachments/assets/225ae759-b4d8-4632-9ee8-b608fb5e4a12">

---

Reach me at: [Email](mailto:hello@tommasomoretti.com) | [Website](https://tommasomoretti.com/?utm_source=github.com&utm_medium=referral&utm_campaign=nameless_analytics) | [Twitter](https://twitter.com/tommoretti88) | [Linkedin](https://www.linkedin.com/in/tommasomoretti/)

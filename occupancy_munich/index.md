# Occupancy munich - Avoid people in corona times


{{<admonition type=quote title="George_Orwell">}}
Big brother is watching you
{{</admonition>}}

{{<figure src= "bubble_chart.gif" title="Weekly overview of the occupancy of a facility">}}


{{< link href="https://howfull.kiesgen.eu" content= "Website (No longer maintained) " >}}

## Introduction

I am a climber and I like to go  **climbing gyms** or **bouldering gyms**. As I and a friend were going regularly to the same gym in Munich, we kept discussing the best possible time we could meet and encounter as few other people as possible. When we had the reluctance to choose our arrival time freely this wasn't a big deal. However, with corona and my friend starting a full-time job, things got complicated. 

Also, it started bothering us that we had the same discussion over and over again, whilst we were waiting in line to get in. That's why we decided to crawl the current occupancy of several gyms in Munich. All this effort to get an informed answer to our question. We create an API and a website to help us and others to find their optimal time to meet at the gym. 

## Website

The website shows the hourly occupancy of the selected facility. The different locations can be selected via the dropdown menu at the top of the page. After the page updates, it shows the occupancy in a bubble chart, which depicts the percentage in size. If over 80%, the colour starts to fade into a red to signal a nearly full facility. The weekly overview should help identify the **peak times** as well as **off-hours**. This view should give an intuitive overview to help plan your gym time in advance.



## API

The project is called *munich-corona-occupancies*. It is a REST API and it is hosted on GitHub. It crawls the current occupancies of climbing, swimming, and sauna facilities in Munich roughly every 15min and commits the data directly to the repo. The API is documented [here](https://zepatrik.github.io/munich-corona-occupancies/).


Fetching the data from the API:

Insert the **gym** and a **date** into the url
```
https://raw.githubusercontent.com/zepatrik/munich-corona-occupancies/main/data/<gym>/<date>.json
```

{{<admonition example "Over 30 facilities" false>}}


| Location ID | Name                            |
|-------------|---------------------------------|
| b_bw_ost    | Boulder Welt Ost                |
| b_bw_sued   | Boulder Welt Süd                |
| b_bw_west   | BoulderWelt West                |
| b_ei        | Einstein                        |
| b_dav_thalk | DAV Thalkirchen Bouldern        |
| k_dav_thalk | DAV Thalkirchen Klettern        |
| b_dav_toelz | DAV Bad Tölz Bouldern           |
| k_dav_toelz | DAV Bad Tölz Klettern           |
| b_dav_freim | DAV Freimann Bouldern           |
| b_dav_gilch | DAV Gilching Bouldern           |
| k_dav_freim | DAV Freimann Klettern           |
| k_dav_gilch | DAV Gilching Klettern           |
| s_cosi      | Cosima Wellness Sauna           |
| s_dante     | Dante Bad Sauna                 |
| s_micha     | Michaeli Bad Sauna              |
| s_nord      | Nordbad Sauna                   |
| s_prinz     | Prinzregentenbad Sauna          |
| s_sued      | Südbad Sauna                    |
| s_volk      | Müller'sches Volksbad Sauna     |
| s_west      | Westbad Sauna                   |
| s_cosima    | Cosima Wellness                 |
| b_forst     | Bad Forstenrieder Park          |
| b_gies      | Bad Giesing-Harlaching          |
| b_michaeli  | Michaeli Bad Schwimmen          |
| b_nord      | Nordbad Schwimmen               |
| b_oly       | Olympia-Schwimmhalle            |
| b_sued      | Südbad Schwimmen                |
| b_volk      | Müller'sches Volksbad Schwimmen |
| b_west      | Westbad Schwimmen               |

{{</admonition>}}


### Some Code Examples

```bash 
  curl https://raw.githubusercontent.com/zepatrik/munich-corona-occupancies/main/data/b_ei/2020-10-28.json
```

```js
var data = fetch('https://raw.githubusercontent.com/zepatrik/munich-corona-occupancies/main/data/b_ei/2020-10-28.json')
  .then(response => response.json())
  .then(data => console.log(data))
```




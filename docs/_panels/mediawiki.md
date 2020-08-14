---
title: Mediawiki
description: contains metrics focused on reviews, including editions, revisions and editors.
author: Bitergia
screenshot: sigils/mediawiki.png
created_at: 
grimoirelab_version: 0.2.0
layout: panel
---

This panel focuses on Mediawiki data source. It shows information about reviews, including  editions, revisions, editors, organizations and projects.


The first visualization, on the left top corner, displays a summary of metrics such as the number of pages, editors and revisions.

Below the metrics visualization, there are two bar charts. The former displays the amount of revisions and new pages based on the time span selected. Furthermore, it also displays the sum of all editions in the wiki.

The latter displays the amount of editors in the time span selected. Thus, the combination of the two visualizations offers useful and complete insights of what happened in a given time span.

In the middle of the panel there are two visualizations, which show organizations information.The visualization at the top displays the different organizations that contributed to mediawiki using a pie chart. It is complemented by a table that contains the amount of editors, revisions and new pages that the organization did.

These two visualizations in combination with filters allow to focus on a given organization, and gives support for comparing organizations.

The table in the top right corner displays the top edited pages (which have a link to the corresponding wiki page), their number of editions and unique editors.

Finally, the last table displays projects data and also the number of editors, revisions and new pages for each organization. Thus, it is useful to complent organizations information.

The tables at the bottom shows the latest events about the latest pages created and edited (e.g., creation date, amount of editions). They support filtering operations and allow to navigate to the corresponding mediawiki pages.

### Files
To use this dashboard with your own GrimoireLab deployment you need to:
* Check [`mediawiki` index][mediawiki-schema] is available on your GrimoireLab instance
(see [grimoirelab-sirmordred documentation][sirmordred-mediawiki] for details on how to deploy it).
* Import the following JSON files using [Kidash tool](https://github.com/chaoss/grimoirelab-kidash/).

| [![Index Pattern][ip-icon]][index-pattern] | | [![Dashboard][dash-icon]][dashboard] |
| :---------: | ---------- | :-------------: |
| **Index Pattern** | ----- | **Dashboard** |

<br />

#### Command line instructions
Once you have the data in place, if you need to manually upload the dashboard execute the
following commands:
```
kidash -e https://user:pass@localhost:443/data --import mediawiki-index-pattern.json
kidash -e https://user:pass@localhost:443/data --import mediawiki.json
```

[mediawiki-schema]: https://github.com/chaoss/grimoirelab-elk/blob/master/schema/mediawiki.csv
[sirmordred-mediawiki]: https://github.com/chaoss/grimoirelab-sirmordred#mediawiki-
[dash-icon]: ../assets/images/icons/dashboard.png
[ip-icon]: ../assets/images/icons/file-ruled.png
[index-pattern]: https://raw.githubusercontent.com/chaoss/grimoirelab-sigils/master/json/mediawiki-index-pattern.json
[dashboard]: https://raw.githubusercontent.com/chaoss/grimoirelab-sigils/master/json/mediawiki.json

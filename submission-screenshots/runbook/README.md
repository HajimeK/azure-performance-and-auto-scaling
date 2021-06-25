# RunBook Screenshots

Here in this RunBook execution, it it triggered by the heavy load on the Kubernetes pods.
When the number of pods increases in those cases, alerts are triggered.
There mails and RunBook are also accompanies.

The resource group used can be seen below.
![](screenshots_see_readme_/2021-06-25-17-08-29.png)

## The alert configuration in Azure Monitor which shows the resource, condition, action group (this should include a reference to your Runbook), and alert rule details (may need 2 screenshots).


![](screenshots_see_readme_/2021-06-25-15-01-23.png)


![](screenshots_see_readme_/2021-06-25-15-04-53.png)



![](screenshots_see_readme_/2021-06-25-15-05-55.png)

### Runbook


## The email you received from the alert when the Runbook was executed.

![](screenshots_see_readme_/2021-06-25-20-53-10.png)

The same alert ID is observed in the cluster alerts.

![](screenshots_see_readme_/2021-06-25-20-56-03.png)

## The summary of the alert which shows 'why did this alert fire?', timestamps, and the criterion in which it fired.

As the workload increases, the number of pods increased.

![](screenshots_see_readme_/2021-06-25-21-19-06.png)

## Runbook executed

![](screenshots_see_readme_/2021-06-25-21-20-21.png)

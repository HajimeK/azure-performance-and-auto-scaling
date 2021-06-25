# RunBook Screenshots

Here in this RunBook execution, it it triggered by the heavy load on the Kubernetes pods.
When the number of pods increases in those cases, alerts are triggered.
There mails and RunBook are also accompanies.

The resource group used can be seen below.
![]((screenshots_see_readme_/2021-06-25-15-47-02.png)

## The alert configuration in Azure Monitor which shows the resource, condition, action group (this should include a reference to your Runbook), and alert rule details (may need 2 screenshots).


![](screenshots_see_readme_/2021-06-25-15-01-23.png)


![](screenshots_see_readme_/2021-06-25-15-04-53.png)



![](screenshots_see_readme_/2021-06-25-15-05-55.png)

### Runbook


## The email you received from the alert when the Runbook was executed.

![](screenshots_see_readme_/2021-06-25-15-11-26.png)

## The summary of the alert which shows 'why did this alert fire?', timestamps, and the criterion in which it fired.

As the workload increases, the number of pods increased.

![](screenshots_see_readme_/2021-06-25-15-12-18.png)

## Runbook executed

![](screenshots_see_readme_/2021-06-25-15-33-35.png)

more details. You can see the runbook was triggered by the pods number increase as designed.

![](screenshots_see_readme_/2021-06-25-15-36-41.png)
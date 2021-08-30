# Auto Scaling VMSS Screenshots

## For the VM Scale Set, create an autoscaling rule based on metrics


Autoscaling Rule
![](screenshots_see_readme_/2021-06-25-12-08-40.png)

## Trigger the conditions for the rule, causing an autoscaling event

Around 1:30pm start making a workload.

Workload script
```
while true; do wget <VMSS external IP> & done
```

CPU utilization
![](screenshots_see_readme_/2021-06-25-14-02-09.png)

When posing a high load, the system scales up automatically as defined.

The number of VMs increased.
![](screenshots_see_readme_/2021-06-25-13-53-44.png)

The instances reached the maximum number defined in the autoscaling rule.
![](screenshots_see_readme_/2021-06-25-13-49-32.png)

After a while since stopped posing a high workload, VM scales down as below.

![](screenshots_see_readme_/2021-06-25-13-54-59.png)

![](screenshots_see_readme_/2021-06-25-14-08-37.png)

## When complete, enable manual scale

![](screenshots_see_readme_/2021-06-25-14-07-21.png)
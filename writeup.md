

https://docs.microsoft.com/en-us/azure-stack/user/azure-stack-dev-start-howto-vm-python?view=azs-2008



## Project Instructions

### Application Insights & Log Analytics

1. Create a Log Analytics workspace resource



2. Create an Application Insights resource and use the Log Analytics workspace created in step 1
3. Enable Application Insights monitoring for the VM Scale Set
4. Add the reference Application Insights to `main.py` and specify the instrumentation key
5. Add custom event telemetry when 'Dogs' is clicked and when 'Cats' is clicked.
6. Create a query to view the event telemetry in Log Analytics.
7. Create a chart from query showing when 'Dogs' or 'Cats' is clicked.

### Monitoring Containers

1. Run `az login` to login, then run `./create-cluster.sh` to create an AKS cluster and deploy a container to it.
2. Once that is completed, go to Insights for the cluster.
3. Observe the state of the cluster. Note the number of nodes and number of containers.
4. Create an alert in Azure Monitor to trigger when the number of pods increases over a certain threshold.
5. Create an autoscaler by using the following Azure CLI command—`kubectl autoscale deployment azure-vote-front --cpu-percent=70 --min=1 --max=10`
6. Cause load on the system
7. After approximately 10 minutes, stop the load.
8. Observe the state of the cluster. Note the number of pods; it should have increased and should now be decreasing.

### Autoscaling

1. For the VM Scale Set, create an autoscaling rule based on metrics.
2. Trigger the conditions for the rule, causing an autoscaling event.
3. When complete, enable manual scale.

### Runbook

1. Create an Azure Automation Account
2. Create a Runbook—either using a script or the UI—that will remedy a problem.
3. Create an alert which uses a runbook to remedy a problem.
4. Cause the problem to the flask app on the VM Scale Set.
5. Verify the problem is remedied via the Runbook.

## Submissions

1. The `main.py` which will show the code for the Application Insights telemety data.
2. Screenshots for the kubernetes cluster which include:
   **Note**: Place all screenshots for Kubernetes Cluster in the `submission-screenshots/kubernetes-cluster` directory
   - The output of the Horizontal Pod Autoscaler, showing an increase in the number of pods.
   - The Application Insights metrics which show the increase in the number of pods.
   - The email you received from the alert when the pod count increased.
3. Screenshots for the Application Insights which include:
   **Note**: Place all screenshots for Application Insights in the `submission-screenshots/application-insights` directory
   - The metrics from the VM Scale Set instance--this will show CPU %, Available Memory %, Information about the Disk, and information about the bytes sent and received. There will be 7 graphs which display this data.
   - Application Insight Events which show the results of clicking 'vote' for each 'Dogs' & 'Cats'
   - The output of the `traces` query in Azure Log Analytics.
   - The chart created from the output of the `traces` query.
4. Screenshots for the Autoscaling of the VM Scale Set which include:
   **Note**: Place all screenshots for Autoscaling VMSS in the `submission-screenshots/autoscaling-vmss` directory
   - The conditions for which autoscaling will be triggered (found in the 'Scaling' item in the VM Scale Set).
   - The Activity log of the VM scale set which shows that it scaled up with timestamp.
   - The new instances being created.
   - The metrics which show the load increasing, then decreasing once scaled up with timestamp.
5. Screenshots for the Azure Runbook which include:
   **Note**: Place all screenshots for RunBook in the `submission-screenshots/runbook` directory
   - The alert configuration in Azure Monitor which shows the resource, condition, action group (this should include a reference to your Runbook), and alert rule details (may need 2 screenshots).
   - The email you received from the alert when the Runbook was executed.
   - The summary of the alert which shows 'why did this alert fire?', timestamps, and the criterion in which it fired.

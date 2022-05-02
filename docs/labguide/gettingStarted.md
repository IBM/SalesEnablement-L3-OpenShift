# Reserving a Cluster

From a web browser, log in to the ITZ at: https://www.ibm.com/it-infrastructure/services/ceccportal/catalog

If this is your first visit to the ITZ, you will first need to agree to the terms and conditions before accessing
the environment.

1. From the Catalog tab, perform a search for **Red Hat OpenShift** and wait for the results to filter.
2. Select the **POWER8 LPAR** bundle by clicking the blue arrow icon of the tile, then wait for the browser to load the configuration page.

   You will now be asked to provide the ITZ with System Details on how you want the environment to be configured.

   Select the I**BM POWER8 LPAR Bundle** you wish to use for the lab. At the time of publishing, that would be the OCP 4.8 pre-install configuration, as shown on the right. If a more recent release of OpenShift is available to you at the time of conducting this lab, you can opt to use the latest release instead. However, be aware that minor changes to the user interface or functionality may arise compared to the instructions provided in this lab guide.

3. Set the **Quantity** equal to _1_ and then click the **Add To Cart** button.

!!! note "Note"

   Deployments of OpenShift on Power through the ITZ are pre-configured in terms of their sizing. By default, CPU, memory, and number of instances provided per deployment are fixed.

   This simplifies the provisioning process in the majority of circumstances (particularly for simple demonstration purposes such as these). However, there may be occasions where you will require a more robust environment — either for your own training or for a client demonstration. If you require a custom configuration, select the **Request Custom Configuration** link as shown.

   Otherwise, there is no configuration required on your part at this stage. We will explore more configuration options in the second half of this lab.

Next you will configure the OpenShift cluster size and reservation period.

4. Click the checkbox for your OCP image request.
5. **Project Name** is set to your own preference.
6. **Used For** is set to _Self Education_.

!!! note "Note"

   Reserve only as much time as you need to complete this lab. You will need an estimate 60 to 90 minutes from start to finish. However, you can safely reserve several days of time if you feel you might benefit from it.

7. When satisfied, click **Reserve Project**.

After configuring the environment (the other variables not mentioned in the previous steps can be left as their default variables), you will be prompted with the following screen.

MISSING image

8. Click **OK** to dismiss.

Pay special attention to the **Date** and **Time** your OCP on PowerVS environment is scheduled for. If you access the Project Kit too early, you’ll only find unresponsive URLs and missing credentials as the cluster is still provisioning.

Wait until an email arrives confirming that your environment is active (which will be sent shortly after your scheduled time slot) before trying to connect to the OpenShift cluster.

# Accessing the ITZ environment

Clicking the Project Kit URL will open a new page for the **Project Kit**, shown below. This page contains all the
details you’ll need to know in order to connect with the OpenShift v4.X cluster.

1. Under the **Offering Information** header (or click P**roject Information** from the tabs) is the Connection URL for your OpenShift cluster. Use this URL to access the cluster.
2. Just below the Connection URL, look for the **Account** and **Password** fields for the Console Credentials. **Record these**. Additional details about your environment are summarized in the headers below. Youcan use this information to work programmatically with the OpenShift cluster — if, for example, you wanted to interact via APIs or an SSH console.
3. Open a new browser tab or window and connect to the OpenShift cluster using the **URL** from **Step 1** and the **credentials** from **Step 2**.

!!! warning "Warning"

   Depending on your browser, you may be presented with a warning similar to the one shown here. Ignore the warning. If you are using Safari, click **Visit This Website** button (as shown) to bypass the warning. You may be asked to enter your **MacOS password** to make the necessary Certificate Trust Settings changes.

!!! note "Note"

   Some users have been prompted to enter the MacOS password twice. Authenticate again if/when instructed to do. When the OpenShift dashboard fully loads, you’ll be ready to advance.

4. Your Web browser will be directed to the OpenShift Container Platform login page. From the two options for login (kube:admin or htpasswd), select the second **htpasswd** button.
5. Enter the credentials provided to you on the Project Kit page for authentication (Step 2 above).

   **Username** is _cecuser_
   **Password** is the string supplied to you on the Project Kit.

6. Click **Log In** when ready and you will be directed to the OpenShift Container Platform web console.

Congratulations — the OCP v4.X cluster is now up and running. You’re ready to get to work.

!!! note "Important"

   Use the accompanying lab guide to complete this course, and remember to record when prompted (with screenshots or in a text log) if asked to do so. You’ll need these logs to pass the certification test.

Refer to the [Certification section](../certificaiton.md) of this document for instructions on how to receive credit for completing this lab.

Good luck!

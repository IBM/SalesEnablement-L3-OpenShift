# Update the deployed application

In this exercise you will directly access the operating system that is running in the container.

1. Return to the OpenShift web console tab/window of your web browser and select **Topology** from the left-hand taskbar.
2. Click the center of the deployment icon to display the deployment side bar containing the deployment details.
3. Click the **Resources** tab and then click on the **pod name** to view more details.

![](_attachments/OCP-deployment-resources-page-3.png)

4. Click the **Terminal** tab.

![](_attachments/OCP-pod-terminal.png)

5. Click inside the **Terminal** window (black box with a prompt like **sh-4.2$**).

The **Terminal** window allows you to issue commands directly to the operating system that is running in the container you deployed using the NGINX image. This image is running a customized Linux operating system.

6. Discover the **hostname** of your NGINX server, by running the **hostname** command.

!!! tip
    To save time, use click the ![](_attachments/CopyToClipboard.png) icon in the sections below to copy the text to your clipboard and then paste the text into the web console.

```
hostname
```

??? example "Example output"
    sh-4.2$ hostname

    nginx-sample-869bf677b6-7wnzs

    sh-4.2$

7. Discover the **IP address** of the running container for your NGINX server, by running the **hostname -i** command.

```
hostname -i
```

??? example "Example output"
    sh-4.2$ hostname -i

    172.30.234.2

    sh-4.2$

Later in this lab you will deploy another NGINX web server and create a load balancer to distribute requests between the two web servers.  To make it easier to identify which web server is being access, change the content that is displayed when you access this server.

8. Issue the following commands in the **Terminal** to modify the web server's default page. You will first create a backup copy of the original file in case you want to revert back to it later.

```
cp index.html index.html.orig
echo NGINX Server 1 works! > index.html
ls
```

??? example "Example output"
    sh-4.2$ cp index.html index.html.orig

    sh-4.2$ echo NGINX Server 1 works! > index.html

    sh-4.2$ ls

    README.md  index.html  index.html.orig  nginx-start  openshift

    sh-4.2$

![](_attachments/OCP-pod-terminal-allcommands.png)

9. Click **Topology** in left-hand task bar of OpenShift web console.
10. Click the **Open URL** button on the edge of the deployment icon. This will launch as a new tab or window in your web browser. You should now see the default page for the web server displays the new message: **NGINX Server 1 works!**

![](_attachments/OCP-server-1-works.png)

In the next section learn about scaling OpenShift containers.

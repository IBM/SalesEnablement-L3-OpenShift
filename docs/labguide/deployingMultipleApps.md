# Deploying multiple instances of an application

Earlier, you learned that a **pod** consists of one or more containers deployed together on **one host**, and is the smallest compute unit that can be defined, deployed, and managed. You also learned you could scale the number of pods up and down which adds a layer of resiliency.  But as noted by the definition of a **pod**, they are running on a single host.  To obtain more resiliency and availability of an application, you can create multiple deployments of an image and load balance traffic to those instances.  In this next section, deploy another instance of the NGINX image.

1. Return to the **Developer** perspective in the OpenShift web console.
2. Click **+Add** in the left-hand taskbar.
3. Click the **View all samples** link on the **Getting started resources** tile.
4. Click the **NGINX** tile.
5. Change the **Name** field from _nginx-sample_ to _nginx-server-2_.
```
nginx-server-2
```
6. Click **Create**.
7. Click **Topology** in left-hand taskbar.
8. Click the center of the newly created **nginx-server-2** deployment.
9. Click the **Resources** tab.
10. Click the name of the running **Pod** to display more information.
11. Click the **Terminal** tab.

Next, change the content of the default page displayed when the NGINX web server is accessed like you did earlier with the first server. This will allow you to easily tell which NGINX deployment you are accessing.

12. Click inside the **Terminal** window (black box with a prompt like **sh-4.2$**).
13. Issue the following commands in the **Terminal** to modify the web server's default page. You will first create a backup copy of the original file in case you want to revert back to it later.

```
cp index.html index.html.orig
echo "NGINX Server 2 works!" > index.html
ls
```

??? example "Example output"
    sh-4.2$ cp index.html index.html.orig
    sh-4.2$ echo NGINX Server 1 works! > index.html
    sh-4.2$ ls
    README.md  index.html  index.html.orig  nginx-start  openshift
    sh-4.2$

14. Click **Topology** in left-hand task bar of OpenShift web console.
15. Click the **Open URL** button on the edge of the _nginx-server-2_ deployment icon. This will launch as a new tab or window in your web browser. You should now see the default page for the web server displays the new message: **NGINX Server 2 works!**

In the next section you will create a route to load balance network traffic between the two NGINX web servers.

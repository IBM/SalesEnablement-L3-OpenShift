# Deploy a containerized application

Using the OpenShift web console you just opened in the [Getting Started section](gettingStarted.md), use the steps below to deploy an **application**. For this lab, the application is a **web server** that is running in a  container running the NGINX image.  NGINX is a free and open-source web server. You can learn more about [NGINX on Wikipedia](https://en.wikipedia.org/wiki/Nginx) and [here](https://www.nginx.com/).


1. In the top-left of the OpenShift web console, locate the **Administrator/Developer** toggle button. You will use this toggle frequently over the course of the hands-on lab to cycle between Administrator and Developer perspectives within the OCP cluster. Select the **Developer** perspective.
2. If not already selected, click the **Project** pull down menu and select the **Project name** created for you. You can find this name in your ITZ reservation e-mail or on the ITZ project page.
3. If not already selected, click the **Add** tab on the left-hand taskbar of the OpenShift web console.
4. Click the **View all samples** link on the **Getting started resources** tile.
5. Click the **NGINX** tile.
6. Change the **Name** field from _nginx-sample_ to _nginx-server-1_.
```
nginx-server-2
```
7. Click **Create**.

Your browser will refresh to the **Topology** view.  Notice the view now shows a NGINX deployment icon. The icon will cycle thru color changes as the container is created and the image is deployed. Wait for the outer circle to turn blue. Once the outer circle is blue, the container can be accessed.

8. Click the **Open URL** button on the edge of the deployment icon to open the default route created during the deployment. This will launch as a new tab or window in your web browser.

!!! Success "Record this!"
    Record the text displayed in the new browser tab/window after you click the **Open URL** button of the NGINX deployment icon.

Your NGINX web server is now alive and well.  Next, learn to scale and manipulate this containerized HTTP server.

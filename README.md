# k6 for monitoring using netdata
# Introduction
This template will help you to integrate K6 and Netdata for monitoring performance test results effectively. K6 is a popular open-source load testing tool that allows us to simulate realistic user traffic, while Netdata provides real-time monitoring and visualisation of system metrics. Combining these two powerful tools enables teams to gain deep insights into application performance and make data-driven decisions. So the template will basically help you to have an integrated framework using K6 and Netdata for effective and realtime monitoring.

# Technologies Used
Performance testing tool - K6

Monitoring tool - Netdata

IDE - IntelliJ Idea

# Prerequisites
K6 should be installed : https://k6.io/docs/getting-started/installation/

Netdata should be installed : https://learn.netdata.cloud/docs/getting-started/install-netdata


# Steps for execution
**1. Clone the repository on your local system by using command** : `git clone https://github.com/knoldus/k6-monitoring-using-netdata.git`


**2. Go to the terminal and execute following commands to launch netdata service**:

Install Netdata using this one liner installer :

`bash <(curl -Ss https://my-netdata.io/kickstart.sh)`


Start your netdata service :

`sudo systemctl start netdata`


Enable netdata to start on boot(optional) :

`sudo systemctl enable netdata`


Access the Netdata web interface : 
* Open a web browser
* Navigate to http://localhost:19999 which is default port to access the Netdata web dashboard for monitoring


**3. Run the load test on K6 and send metrics to Netdata**:

`sudo k6 run --out statsd myScript.js`

here myScript.js contains k6 script for performance testing of an API but you can alter it according to your requirments.

**4. Monitor performance with Netdata** :

Open your web browser again and navigate to your Netdata instance’s URL (e.g., http://localhost:19999) or refresh the existing browser where the Netdata dashboard opened.



For a better understanding and changing this project according to you please refer to this blog based on same:-
https://blog.nashtechglobal.com/wp-admin/post.php?post=5073&action=edit

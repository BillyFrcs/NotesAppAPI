<h1 align="center">Notes App API | Back-End</h1>

Testing to Deployed a [Node.js](https://nodejs.org) Back-End Notes App API in Google Cloud Platform with Google Compute Engine Virtual Machine (VM) Instances.

## Setup And Installation 

* Run `npm install` to install all of the required dependencies.
* Start the server in Production mode run `npm run start` and to start in Development mode just simply run `npm run dev` that's pretty much it.

> <b>Note:</b> Make sure that `disable` the value of <b>Block insecure private network</b> in `chrome://flags` to avoid <b>Same-Origin Policy</b> problems in browser. After that don't forget to set it back to the `default` value.


## Google Cloud Console
Go to [Google Cloud Console](https://console.cloud.google.com/) and create a firewall rule and VM instance.

1. Create a firewall rule <b>Navigation menu > VPC network > Firewall</b>

| Properties         | Values                                                |
|--------------------|-------------------------------------------------------|
| Name               | app-server-firewall                                   |
| Paragraph          | Allow Custom TCP Port 5000                            |
| Targets            | Specified target tags                                 |
| Target tags        | web-server                                            |
| Source filter      | IPv4 ranges                                           |
| Source IPv4 ranges | 0.0.0.0/0                                             |
| Protocol and ports | Specified protocols and ports > check tcp > fill 5000 |

2. Create a VM Instance <b>Navigation menu > Compute Engine</b>

| Properties    | Values                             |
|---------------|------------------------------------|
| Name          | web-server                         |
| Region        | asia-southeast2 (Jakarta)          |
| Zone          | asia-southeast2-a                  |
| Machine type  | e2-micro (2 vCPU, 1 GB memory)     |                                      
| Boot disk     | Type: New balanced persistent disk | 
|               | Size: 10 GB                        |
|               | Image: Ubuntu 20.04 LTS            |

> Test the Back-End System in [here](http://notesapp-v1.dicodingacademy.com/)

<h1 align="center">Notes App | Back-End</h1>

Testing to Deployed a [Node.js](https://nodejs.org) Back-End Notes App in Google Cloud Platform with Google Compute Engine Virtual Machine (VM) Instances.

<h2>Setup And Installation</h2>

* Run `npm install` to install all of the required dependencies.
* Start the server in Production mode run `npm run start` and to start in Development mode run `npm run dev`
* Google Cloud Console setup 
1. Create a firewall rule `Navigation menu > VPC network > Firewall`
| Properties         | Value                                                 |
| ------------------ | ------------------                                    |       
| Name               | app-server-firewall                                   |
| Paragraph          | Allow Custom TCP Port 5000                            |
| Targets            | Specified target tags                                 |
| Target tags        | web-server                                            |
| Source filter      | IPv4 ranges                                           |
| Source IPv4 ranges | 0.0.0.0/0                                             |
| Protocol and ports | Specified protocols and ports > check tcp > fill 5000 |

> Test the Back-End System in [here](http://notesapp-v1.dicodingacademy.com/)
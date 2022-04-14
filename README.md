# Server for Unciv written in Python

It's a simple webserver for Unciv that uses the Python built in http.server module.

## Installation

Make sure you have Python3 installed.
The server was tested with Python 3.9 and 3.10.

Use [git](https://git-scm.com) to download the Unciv_server

```bash
mkdir Unciv_server
cd Unciv_server
git clone https://github.com/Mape6/Unciv_server.git
```

## Usage

```
usage: Unciv_server.py [-h] [-p PORT] [-l {CRITICAL,ERROR,WARNING,INFO,DEBUG}] [-s]

This is a simple HTTP webserver for Unciv

optional arguments:
  -h, --help            show this help message and exit
  -p PORT, --port PORT  Specifies the port on which the server should listen (default: 80)
  -l {CRITICAL,ERROR,WARNING,INFO,DEBUG}, --log-level {CRITICAL,ERROR,WARNING,INFO,DEBUG}
                        Change logging level (default: WARNING)
  -s, --ssl             Starts a HTTPS server instead of HTTP
```

To start an HTTPS server on 443:
```
./Unciv_server.py -p 443 -s
```

The SSL support is very rudimentary and the certificate is self-signed. Don't make the server directly reachable from the internet.
I strongly recommend to use a reverse proxy in front of this webserver to take care of the certificate and termination of the SSL sessions.

I tested the connection with Android 12 and Unciv 4.0.6. The app crashes immediately...

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## License
This project is [MPL-2.0](https://github.com/Mape6/Unciv_server/blob/main/LICENSE) licensed.

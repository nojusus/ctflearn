Opening the "data.pcap" file in Wireshark and searching for any HTTP method, a POST method can be found and traced along with Right Click > Follow > TCP Stream and locating the password. The password is under a base64 encoding, but contains a wrong tail. The first step is to change the tail from "%3D%3D" to "==" to get a decodable string. Finally, decoding the string with
```bash
echo "UEFwZHNqUlRhZQ==" | base64 -d
```
produces a string, that you can wrap inside the most common flag prefix to produce the actual flag.

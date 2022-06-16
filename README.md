# simple-http-server

Simple http server using python3's built-in http.server module with a PUT extenstion to be able to upload/send files to a hosting server quickly.

## How-to

1) Run `main.py` on your server machine that should receive files
1) Test locally: `curl -i -X PUT --upload-file path/to/your/file.txt http://localhost:8000`

## Known issues

### Blocked firewall

In case the port 8000 is blocked in your firewall, you have to open it.

For example, on RHEL/CentOS/Fedora, open port 8000 as shown below.

```
$ firewall-cmd --permanent --add-port=8000/tcp
$ firewall-cmd --reload
```

On Debian, Ubuntu you can allow the port as shown below.

`$ sudo ufw allow 8000`

## References

* [https://stackoverflow.com/questions/39788591/python-simplehttpserver-to-receive-files](https://stackoverflow.com/questions/39788591/python-simplehttpserver-to-receive-files)

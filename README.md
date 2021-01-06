# JNA/JNI
When we need to call the c/c++ program, it is JNA/JNI that we need to complete.


## Kill the progresses of the same PGID
You can kill the progresses, parent, children and grandchildren which are of the same PGID

```sh
PGID=`ps j -A | grep 'xxxxx' | grep -v 'grep' | awk '{print  $3}'`
kill -SIGTERM -- -${PGID}
```
* set the progress [PGID](https://man7.org/linux/man-pages/man2/setpgid.2.html) and [SID](https://man7.org/linux/man-pages/man2/setsid.2.html)
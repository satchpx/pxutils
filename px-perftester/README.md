# Portworx Performance Test Runner
**The test container uses fio and iostat**  

## To run the performance tester
On the target machine, run:
~~~
mkdir -p /tmp/fio-results
docker run --rm --volume-driver pxd -v /tmp/fio-results:/tmp/fio-results -v size=100G,repl=1,name=fio-test-vol:/mnt satchpx/px-perftester:1.0.0
~~~

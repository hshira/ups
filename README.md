Universal Proxy Service: UPS
===

UPS is a RESTful service that --

* Provides capability to introduce latency in response time to any service via a parameter on the URL. Example:  https://localhost:8081/ups-svc?delay=1000ms)
* Provides capability to return error responses specified by errorCode and errorRate as below.  Example:  https://localhost:8081/ups-svc?errorRate=50%&errorCode=503


Future plan
* Make ups capable for service-mutation-testing. Faults (or mutations) will be automatically seeded into your REST calls, then your tests are run. If your tests fail then the mutation is killed, if your tests pass then the mutation lived. This is similar to the Pi Test http://pitest.org/ , the only difference being that PiTest works on the code in same JVM whereas UPS will work as a proxy for external services.



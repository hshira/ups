ups
===
UPS should be callable by a service via a REST endpoint
UPS should provide a capability to introduce latency in response time to any service via a parameter on the URL. (e.g. https://ups.test.intuit.com/ups-svc?delay=1000ms)
UPS should provide a capability to return error responses specified by errorCode and errorRate as below --https://ups.test.intuit.com/ups-svc?errorRate=50%&errorCode=503
UPS should be extendable to do service-mutation-testing. Faults (or mutations) will be automatically seeded into your REST calls, then your tests are run. If your tests fail then the mutation is killed, if your tests pass then the mutation lived. This is similar to the Pi Test http://pitest.org/ , the only difference being that PiTest works on the code in same JVM whereas UPS will work as a proxy for external services.

Universal Proxy Service


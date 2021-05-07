# 🌽
## Milho Tests

This repo contains tests for implementations of the milho language. Those tests are intended to test the correctness of a milho implementation.
For the tests to run you need to have the following function already injected on the scope of your milho. And all of the builtins or types this function needs.
```
(defn test (name expected result)
	(if (= expected result)
		(println "PASS:" name)
		(progn
			(println "FAIL:" name)
			(println "  └─ Value {" (str result) "} doesn't equal expected result {" (str expected) "}."))))

```
### Running the tests
You will need to pass as the first argument, the full path of your milho "binary". This "binary" needs to read the milho source file passed as it's first argument.
```./your-milho current-test.milho```

If you don't pass the path to a binary, the script will test the milho available on your path.
```sh
# With the binary
./run ~/Projects/milho/milho

# or

./run
```
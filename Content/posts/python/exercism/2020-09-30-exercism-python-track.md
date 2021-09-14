---
date: "2020-09-30T00:00:00Z"
title: exercism Python track
---
I am working through Exercism's [Python Track](https://exercism.io/my/tracks/python) coding practice. 

## Setup
Exercism uses a command-line client as a link between the website and our local work. Latest releases of the client is available at https://github.com/exercism/cli. Arch/Manjaro Linux binary package is available at the Arch User Repository, [exercism](https://aur.archlinux.org/packages/exercism/) or [exercism-bin](https://aur.archlinux.org/packages/exercism-bin/).

``` shell
# yay is an Arch User Repository (AUR) helper 
# get it from https://github.com/Jguer/yay

> yay -Ss exercism
aur/exercism 3.0.13-1 (+6 0.72) 
    Command line client for https://exercism.io
aur/exercism-bin 3.0.13-2 (+69 1.73) 
    Command line client for exercism.io

> yay -S exercism-bin # prebuilt binary, doesn't require golang

> yay -Ql exercism-bin
exercism-bin /usr/
exercism-bin /usr/bin/
exercism-bin /usr/bin/exercism
...

> exercism help

> exercism configure --workspace ~/Exercism

# [Python | Hello World | Exercism](https://exercism.io/my/solutions/04bcc66509104f5c91ccb6cc39280a64)
> exercism download --exercise=hello-world --track=python
```

## Hello World

``` python
# pytest hello_world_test.py 
F                                                                                            [100%]
============================================= FAILURES =============================================
____________________________________ HelloWorldTest.test_say_hi ____________________________________

self = <hello_world_test.HelloWorldTest testMethod=test_say_hi>

    def test_say_hi(self):
>       self.assertEqual(hello(), "Hello, World!")
E       AssertionError: None != 'Hello, World!'

hello_world_test.py:10: AssertionError
===================================== short test summary info ======================================
FAILED hello_world_test.py::HelloWorldTest::test_say_hi - AssertionError: None != 'Hello, World!'
1 failed in 0.06s

# hello_world.py

def hello():
    return 'Hello, World!'

# pytest hello_world_test.py 
.                                                                                            [100%]
```

"Hello, World!" is the traditional first program, when learning a new language. We wrote a `hello` function which returns the string and ran the test suite using [pytest](https://docs.pytest.org/en/stable/) to check we are correct. We need to submit our solution using the `exercism` command. 

``` shell
exercism submit hello_world.py

    Your solution has been submitted successfully.
    You can complete the exercise and unlock the next core exercise at:

    https://exercism.io/my/solutions/04bcc66509104f5c91ccb6cc39280a64
```

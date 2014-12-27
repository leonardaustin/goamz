# goamz - An Amazon Library for Go

[![Build Status](http://travis-ci.org/leonardaustin/goamz.png?branch=master)](https://travis-ci.org/leonardaustin/goamz)

The _goamz_ package enables Go programs to interact with Amazon Web Services.

This is a fork of the version [developed within Canonical](https://wiki.ubuntu.com/goamz) with additional functionality and services from [a number of contributors](https://github.com/leonardaustin/goamz/contributors)!

The API of AWS is very comprehensive, though, and goamz doesn't even scratch the surface of it. That said, it's fairly well tested, and is the foundation in which further calls can easily be integrated. We'll continue extending the API as necessary - Pull Requests are _very_ welcome!

The following packages are available at the moment:

```
github.com/leonardaustin/goamz/autoscaling
github.com/leonardaustin/goamz/aws
github.com/leonardaustin/goamz/cloudformation
github.com/leonardaustin/goamz/cloudfront
github.com/leonardaustin/goamz/cloudwatch
github.com/leonardaustin/goamz/dynamodb
github.com/leonardaustin/goamz/ec2
github.com/leonardaustin/goamz/elb
github.com/leonardaustin/goamz/iam
github.com/leonardaustin/goamz/rds
github.com/leonardaustin/goamz/route53
github.com/leonardaustin/goamz/s3
github.com/leonardaustin/goamz/sqs
github.com/leonardaustin/goamz/sts

github.com/leonardaustin/goamz/exp/mturk
github.com/leonardaustin/goamz/exp/sdb
github.com/leonardaustin/goamz/exp/sns
```

Packages under `exp/` are still in an experimental or unfinished/unpolished state.

## API documentation

The API documentation is currently available at:

[http://godoc.org/github.com/leonardaustin/goamz](http://godoc.org/github.com/leonardaustin/goamz)

## How to build and install goamz

Just use `go get` with any of the available packages. For example:

* `$ go get github.com/leonardaustin/goamz/ec2`
* `$ go get github.com/leonardaustin/goamz/s3`

## Running tests

To run tests, first install gocheck with:

`$ go get github.com/motain/gocheck`

Then run go test as usual:

`$ go test github.com/leonardaustin/goamz/...`

_Note:_ running all tests with the command `go test ./...` will currently fail as tests do not tear down their HTTP listeners.

If you want to run integration tests (costs money), set up the EC2 environment variables as usual, and run:

$ gotest -i

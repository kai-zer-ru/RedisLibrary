# ABOUT

Library to work with [redis] (http://redis.io) in language [Go] (http://golang.org/). 

It requires [redigo] (https://github.com/garyburd/redigo/) 

Refinement still in the process, write basic functions.

## Author

Kaizer666 - [http://vk.com/](http://vk.com/id42002307)

## Install

    go get github.com/kaizer666/RedisLibrary
    
## Use

<pre>

package main

import (
      "github.com/kaizer666/RedisLibrary"
      "fmt"
      )

func main() {
    MyRedis := RedisLibrary.RedisType{
        Host:"localhost",
        Port:1234,
        Password:"qweqweqweqw",// Необязательный параметр
        DB:0,// Необязательный параметр
        }
    MyRedis.Connect()
    defer MyRedis.Close()
    row,err := MyRedis.HGetAll("TestSetKey")
    if err != nil {
        panic(err)
    }
    fmt.Println(row)
}

</pre>




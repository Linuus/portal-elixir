Portal
======

How to run it locally

```iex
$ iex -S mix
iex(1)> Portal.shoot(:blue)
{:ok, #PID<0.88.0>}
iex(2)> Portal.shoot(:orange)
{:ok, #PID<0.89.0>}
iex(3)> portal = Portal.transfer(:blue, :orange, [1,2,3,4])
#Portal<
       :blue <=> :orange
[1, 2, 3, 4] <=> []
>
iex(4)> Portal.push_right(portal)
#Portal<
    :blue <=> :orange
[1, 2, 3] <=> [4]
>
iex(5)> Portal.push_right(portal)
#Portal<
 :blue <=> :orange
[1, 2] <=> [3, 4]
>
```

TODO:
- Example of running on distributed nodes.
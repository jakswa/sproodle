# Rouse

This is a barebones attempt at cloning NPM's concurrently package.

![image](https://user-images.githubusercontent.com/137793/194436290-8cff0e89-e01e-4ce9-a156-974e0e4913da.png)

## Examples

1. With command line arguments
```shell
$ cargo install rouse
$ rouse "echo 'wow cool'" "sleep 2; echo 'also cool'"
[echo] wow cool
[sleep] also cool
```

2. With `cmds.toml` TOML file in your directory.

```toml
[[cmds]]
label = "wtf"
cmd = "sleep 4; echo 'fuck yeah'"

[[cmds]]
label = "wtf2"
cmd = "sleep 2; echo 'fuck yeah'"
```

```shell
$ rouse
[wtf2] fuck yeah
[wtf] fuck yeah
```



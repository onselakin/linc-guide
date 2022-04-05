# Adding interactive content

As you already know by now, the steps can contain interactive content in the form of executable commands and questions that can provide hints and solutions. Let's take a look at how this works.

## Executable shell commands

Normally, we use the default Markdown extensions to alert the user that the text is a code snippet, like below:

```text
    ```bash
    ls -al
    ```
```

You add interactivity to the snippets by using the special syntax:

```text
    ```bash
    ~{
        title: Sample shell command
        executable: true
    }~
    ls -al
    ```
```

This creates the output shown below:

```bash
~{
    title: Sample shell command
    executable: true
}~
ls -al
```

You can also let users try to guess the commands by hiding them and giving hints so that they've a more interactive learning experience instead of just reading.

```text
    ```bash
    ~{
        title: Create an nginx deployment
        executable: true
        targetTerminal: some-id
        hint: You need to use kubectl to make this work!
    }~
    kubectl create deployment nginx --image=nginx
    ```
```

This is how the snippet renders:

```bash
~{
  title: Create an nginx deployment
  executable: true
  targetTerminal: default-terminal-id
  hint: You need to use kubectl to make this work!
}~
kubectl create deployment nginx --image=nginx
```

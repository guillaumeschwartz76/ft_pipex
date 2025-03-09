# ft_pipex

This project involves the detailed discovery of a UNIX mechanism : PIPE, REDIRECTION and HEREDOC

## Installing and Compiling ft_pipex

Clone the repository

```shell
https://github.com/guillaumeschwartz76/ft_pipex.git
```

You can go to the directory for compilation and can do ```make```.

## Executing ft_pipex

This program need a file, a first command, a second command and outfile.
The program will try to open the first file and then execute the first command.
then, as with a pipe, it retrieves the result, applies the second command and
transfers the result to the output file.

It will look like the following shell command:
```shell
< file1 cmd1 | cmd2 > file2
```

```shell
./pipex <file1> <cmd1> <cmd2> <file2>
```

## Installing, Compiling and Executing the bonus

The program features a bonus section that will allow an unlimited number of pipes,
as well as heredoc management.

In the same directory you can do ```make bonus```.

Now you can use an unlimited number of commands separated by pipes:
```shell
./pipex_bonus <file1> <cmd1> ... <cmd2> <file2>
```

You can now also use a heredoc instead of the input file followed by are delimiter, but you can use only two command:
```shell
 ./pipex here_doc LIMITER cmd cmd1 file
 ```

It will look like the following shell command:
```shell
cmd << LIMITER | cmd1 >> file
```
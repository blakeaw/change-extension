# change-extension

Defines a Bash script `chext` that can change the extension of all files with a given extension.

## Install

If you have `sudo` access you use the provided install script which will place `chext` in `/usr/local/bin`:

```shell
sudo bash install.sh
```

Otherwise, you can copy `chext` to some other local location in your `PATH` and make it executable with `chmod`:

```shell
cp ./chext ~/location/in/PATH/
chmod u+x ~/location/in/PATH/chext
```

## Usage

Change the extension of files in the current directory from `foo` to `bar`:

```shell
chext foo bar
```

Results in 

`alpha.foo beta.foo`

changed to

`alpha.bar beta.bar`

### Recursive with -r

Make the change recursively down from the current directory using the `-r` flag:

```shell
chext -r foo bar
```

Results in 

`./alpha.foo ./beta.foo ./sub1/delta.foo`

changed to

 `./alpha.bar ./beta.bar ./sub1/delta.bar`
# police
A module dependency version policing tool. It goes through all your repositories on github which has package.json.
Then it analyzes the dependencies and reports back to you about all the outdated packages.

It also can suggest corrections to your package.json file in certain cases.

## Installation
Install police globally from npm registry by typing the following command

```
npm install police -g
```

## Usage
For the first time after you installed police, you need to authenticate yourself to [github](github.com).
This is a one-time step

```
police auth
```

**Note:** We will not save your [github](github.com) password anywhere. A token which we acquire during
the authentication will be used thereafter.

```sh
# To police your module dependencies
police

# To police a particular module (You should give the repository name)
police octonode

# To police another user/org module dependencies
police -u flatiron

# To police a particular module of another user/org (You should give the repository name)
police flatiron/plates
```

The token which we acquied during auth will be stored in `$HOME/.policeconf`. If you want to use another config file

```
police octonode --conf /etc/policeconf
police octonode --conf ~/.conf
```

If you want to destory your token, you can use

```
police -d
police --destroy
```

Calling police with help option will display all the above

```
police -h
police --help
```

## Testing
```
npm test
```

## Contributors
[Contributors](http://github.com/pkumar/nocof/contributors)

## License
MIT/X11

## Bug Reports
Report [here](http://github.com/pkumar/nocof/issues)

## Contact
Pavan Kumar Sunkara (pavan.sss1991@gmail.com)

Follow me on [github](https://github.com/users/follow?target=pkumar), [twitter](http://twitter.com/pksunkara)

Concept by: Martin Wawrusch (martin@wawrusch.com)

# starttls-policy Python package

## Package API

## Run CLI
Since this is a developer alpha, we recommend using `virtualenv` and `pip` to
install and run `starttls-policy`. To get set up:
```
virtualenv --no-site-packages --setuptools venv --python python2.7
source ./venv/bin/activate
pip install starttls-policy
```

If you are getting the following error when installing via pip:

```
Collecting starttls-policy
  Could not find a version that satisfies the requirement starttls-policy (from versions: )
No matching distribution found for starttls-policy
```

then run the following instead, in order to get the module installed:

```
$ git clone https://github.com/EFForg/starttls-everywhere.git 
$ cd starttls-everywhere/starttls-policy
$ python setup.py install
```


#### Manually updating the policy list
The below will fetch the remote policy list from `https://dl.eff.org/starttls-everywhere/policy.json` and verify the corresponding signature:
```
starttls-policy --update-only [--policy-dir /path/to/dir]
```

#### Generating a configuration file
`starttls-policy --generate <MTA> [--policy-dir /path/to/dir]` will generate a configuration file corresponding to the TLS policy list and provide instructions for installing the file.

We currently only support Postfix, but contributions are welcome!


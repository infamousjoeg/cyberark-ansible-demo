# Loading Conjur Security Policy

Add the following to your existing `root.yml` root policy:

```yaml
- !policy
  id: ansible-tower
  owner: !group /admins
```

Then load the root policy in the root namespace:

`$ conjur policy load root root.yml`

Now, you can load your `ansible-tower.yml` policy under the ansible-tower namespace:

`$ conjur policy load ansible-tower ansible-tower.yml`

This will output a JSON response.  Save this blob!  It contains your host ID and API key.

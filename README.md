# GitHub Action - Adding Debian repo definitions of Frank Brehm

Adding Debian repo definitions of Frank Brehm

It may be only used by Debian or Ubuntu based images.

It performs the following steps:

* Updating the Debian repo information
* Creating a new Debian source list file with one entry for the Debian package repo of Frank Brehm
* Updating the Debian repo information again

## Example

```yaml

    steps:

      - name: 'Adding Debian repo definitions of Frank Brehm'
        uses: fbrehm/github-add-fb-debian-repo@main
        with:
          vendor: Debian
          distro: bookworm

```

## Inputs

```yaml
inputs:
  use_https:
    description: 'Use HTTPS instead of HTTP as the URL schema.'
    type: boolean
    required: false
    default: false
  repo_server:
    description: 'The FQDN of the repository server.'
    required: false
    type: string
    default: 'repo.uhu-banane.de'
  root_path:
    description: 'The root path on the repository server.'
    required: false
    type: string
    default: '/'
  gpg_key_path:
    description: 'The path to the GPG key of the repository on the repo server.'
    required: false
    type: string
    default: 'public/repo.uhu-banane.de.gpg-key2.asc'
  vendor:
    description: 'The main Debian vendor (Debian or Ubuntu).'
    required: true
    type: string
  distro:
    description: 'The distribution of the vendor (buster, focal, bullshead a.s.o.)'
    required: true
    type: string
  suite:
    description: 'The suite of the distribution'
    required: false
    type: string
    default: './'
```


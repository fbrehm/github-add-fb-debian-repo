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


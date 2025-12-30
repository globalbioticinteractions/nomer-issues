# Nomer Issues

GitHub help facilitate open source development through git, a distributed revision control system. 

Aside from version control through git repositories, GitHub offers issue tracking. 

This repository keeps track of issues for Nomer (a GloBI tools), a project that supports mapping (mainly taxonomic) terms to other terms. The aim of this repository is to keep track of GloBI related communication by making them available through ... a git repository.

## Methods 

The github issues and their associated attachments are tracked by periodically executing the following command 

```bash
# optionally set token to increase api limits. 
export GITHUB_TOKEN=[your personal github token] 

# track the issues
preston track https://github.com/globalbioticinteractions/nomer/issues
```

## Results 

After tracking the issues, each issue and their associated comment is available in json format. 

The example below prints the content associated with [issue #1](https://github.com/globalbioticinteractions/nomer/issues/1) of [Global Biotic Interactions](https://github.com/globalbioticinteractions/nomer) using preston, grep and jq.

```
preston head \
 | preston cat \
 | grep hasVersion \
 | grep -E "https://api.github.com/repos/.*/issues/1[^0-9]"
 | preston cat 
```

yielding the following result retrieved from 

```
```


```
```

```
```


```
```

## Discussion

By tracking GitHub issues and versioning their content, we can now access issues without being constrained by GitHub API rate limits. Also, the associated content can now be accessed and processed outside the GitHub platform without putting pressure on the GitHub API services.
 


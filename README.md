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
<https://api.github.com/repos/globalbioticinteractions/nomer/issues/1> <http://purl.org/pav/hasVersion> <hash://sha256/eae60a4d2882e7efc6f0b83ef4f6e66a668bcf8ac78b8069197f2eb878f3a050> <urn:uuid:b679e8a4-f92f-44ac-a0a6-342eb3f4bcce> .
<https://api.github.com/repos/globalbioticinteractions/nomer/issues/1/comments?per_page=100> <http://purl.org/pav/hasVersion> <hash://sha256/27d50fa6b9d6eff7f6343bce4cc38af5e730dc83aa0026e5155d348658ad2dd9> <urn:uuid:8383836b-014d-4dae-b2b6-7251faf32b65> .
```


```
{
  "url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/1",
  "repository_url": "https://api.github.com/repos/globalbioticinteractions/nomer",
  "labels_url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/1/labels{/name}",
  "comments_url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/1/comments",
  "events_url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/1/events",
  "html_url": "https://github.com/globalbioticinteractions/nomer/issues/1",
  "id": 293368902,
  "node_id": "MDU6SXNzdWUyOTMzNjg5MDI=",
  "number": 1,
  "title": "allow schema definition for terms and term maps",
  "user": {
    "login": "jhpoelen",
    "id": 1084872,
    "node_id": "MDQ6VXNlcjEwODQ4NzI=",
    "avatar_url": "https://avatars.githubusercontent.com/u/1084872?v=4",
    "gravatar_id": "",
    "url": "https://api.github.com/users/jhpoelen",
    "html_url": "https://github.com/jhpoelen",
    "followers_url": "https://api.github.com/users/jhpoelen/followers",
    "following_url": "https://api.github.com/users/jhpoelen/following{/other_user}",
    "gists_url": "https://api.github.com/users/jhpoelen/gists{/gist_id}",
    "starred_url": "https://api.github.com/users/jhpoelen/starred{/owner}{/repo}",
    "subscriptions_url": "https://api.github.com/users/jhpoelen/subscriptions",
    "organizations_url": "https://api.github.com/users/jhpoelen/orgs",
    "repos_url": "https://api.github.com/users/jhpoelen/repos",
    "events_url": "https://api.github.com/users/jhpoelen/events{/privacy}",
    "received_events_url": "https://api.github.com/users/jhpoelen/received_events",
    "type": "User",
    "user_view_type": "public",
    "site_admin": false
  },
  "labels": [
    {
      "id": 801028350,
      "node_id": "MDU6TGFiZWw4MDEwMjgzNTA=",
      "url": "https://api.github.com/repos/globalbioticinteractions/nomer/labels/enhancement",
      "name": "enhancement",
      "color": "84b6eb",
      "default": true,
      "description": "New feature or request"
    }
  ],
  "state": "closed",
  "locked": false,
  "assignee": null,
  "assignees": [],
  "milestone": null,
  "comments": 1,
  "created_at": "2018-02-01T01:07:40Z",
  "updated_at": "2019-12-25T00:41:43Z",
  "closed_at": "2019-12-25T00:41:42Z",
  "author_association": "MEMBER",
  "type": null,
  "active_lock_reason": null,
  "sub_issues_summary": {
    "total": 0,
    "completed": 0,
    "percent_completed": 0
  },
  "issue_dependencies_summary": {
    "blocked_by": 0,
    "total_blocked_by": 0,
    "blocking": 0,
    "total_blocking": 0
  },
  "body": "Currently, term caches and term maps have to have specific column header for nomer to work with the ```globi-cache``` matcher. \r\n\r\nFor instance, a term cache should contain the header labels ```id``` and ```path```. Also, a term map has to contain headers ```providedTaxonId```, ```providedTaxonName```, ```resolvedTaxonId``` and ```resolvedTaxonName```. \r\n\r\nSuggest to adopt method to define the columns in which term id / labels and related mappings can be found. ",
  "closed_by": {
    "login": "jhpoelen",
    "id": 1084872,
    "node_id": "MDQ6VXNlcjEwODQ4NzI=",
    "avatar_url": "https://avatars.githubusercontent.com/u/1084872?v=4",
    "gravatar_id": "",
    "url": "https://api.github.com/users/jhpoelen",
    "html_url": "https://github.com/jhpoelen",
    "followers_url": "https://api.github.com/users/jhpoelen/followers",
    "following_url": "https://api.github.com/users/jhpoelen/following{/other_user}",
    "gists_url": "https://api.github.com/users/jhpoelen/gists{/gist_id}",
    "starred_url": "https://api.github.com/users/jhpoelen/starred{/owner}{/repo}",
    "subscriptions_url": "https://api.github.com/users/jhpoelen/subscriptions",
    "organizations_url": "https://api.github.com/users/jhpoelen/orgs",
    "repos_url": "https://api.github.com/users/jhpoelen/repos",
    "events_url": "https://api.github.com/users/jhpoelen/events{/privacy}",
    "received_events_url": "https://api.github.com/users/jhpoelen/received_events",
    "type": "User",
    "user_view_type": "public",
    "site_admin": false
  },
  "reactions": {
    "url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/1/reactions",
    "total_count": 0,
    "+1": 0,
    "-1": 0,
    "laugh": 0,
    "hooray": 0,
    "confused": 0,
    "heart": 0,
    "rocket": 0,
    "eyes": 0
  },
  "timeline_url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/1/timeline",
  "performed_via_github_app": null,
  "state_reason": "completed"
}
[
  {
    "url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/comments/568814666",
    "html_url": "https://github.com/globalbioticinteractions/nomer/issues/1#issuecomment-568814666",
    "issue_url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/1",
    "id": 568814666,
    "node_id": "MDEyOklzc3VlQ29tbWVudDU2ODgxNDY2Ng==",
    "user": {
      "login": "jhpoelen",
      "id": 1084872,
      "node_id": "MDQ6VXNlcjEwODQ4NzI=",
      "avatar_url": "https://avatars.githubusercontent.com/u/1084872?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/jhpoelen",
      "html_url": "https://github.com/jhpoelen",
      "followers_url": "https://api.github.com/users/jhpoelen/followers",
      "following_url": "https://api.github.com/users/jhpoelen/following{/other_user}",
      "gists_url": "https://api.github.com/users/jhpoelen/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/jhpoelen/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/jhpoelen/subscriptions",
      "organizations_url": "https://api.github.com/users/jhpoelen/orgs",
      "repos_url": "https://api.github.com/users/jhpoelen/repos",
      "events_url": "https://api.github.com/users/jhpoelen/events{/privacy}",
      "received_events_url": "https://api.github.com/users/jhpoelen/received_events",
      "type": "User",
      "user_view_type": "public",
      "site_admin": false
    },
    "created_at": "2019-12-25T00:41:42Z",
    "updated_at": "2019-12-25T00:41:42Z",
    "body": "has been implemented. ",
    "author_association": "MEMBER",
    "reactions": {
      "url": "https://api.github.com/repos/globalbioticinteractions/nomer/issues/comments/568814666/reactions",
      "total_count": 0,
      "+1": 0,
      "-1": 0,
      "laugh": 0,
      "hooray": 0,
      "confused": 0,
      "heart": 0,
      "rocket": 0,
      "eyes": 0
    },
    "performed_via_github_app": null
  }
]
```

## Discussion

By tracking GitHub issues and versioning their content, we can now access issues without being constrained by GitHub API rate limits. Also, the associated content can now be accessed and processed outside the GitHub platform without putting pressure on the GitHub API services.
 


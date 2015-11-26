# circle ci test

configure the project on circle, add `GITHUB_ACCESS_TOKEN` env var
(needed for publishing new release)

## cut release

```sh
# trigger build with release type
$ curl -H 'Content-Type: application/json' \
       --data '{"build_parameters":{"RELEASE_TYPE":"patch"}}' \
       'https://circleci.com/api/v1/project/madbence/circle/tree/master?circle-token=$CIRCLE_TOKEN'
```

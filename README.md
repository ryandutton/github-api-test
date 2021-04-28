# github-api-test
Testing the Github REST API to see what can be done

## Test 1
Created a new branch on the terminal, made changes to the readme then pushed the new branch to the repo. I then manually create the pull request on the GUI. Fianlly I confirmed that the pull request can be idenfitied using the following command

```bash
curl \
  -X GET \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/octocat/hello-world/pulls
```

## Test 2
Creating the pull request using the api using POST /pulls endpoint and then confirming that the pull request was successfully created on the GUI

```bash
curl \
  -X POST \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/octocat/hello-world/pulls \
  -d '{"title": "Pull Request Name", "body": Description for pull request", "head":"test-branch-2","base":"main"}'
```

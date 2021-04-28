# github-api-test
Testing the Github REST API to see what can be done

## Test 1
Created a new branch to list pull requests which are open.

## Test 2
Creating the pull request using the api using POST /pulls endpoint

`e.g.

curl \
  -X POST \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/octocat/hello-world/pulls \
  -d '{"head":"test-branch-2","base":"main"}'
`

# trivy-pr-report

Fail the build if security vulnerabilities of HIGH or CRITICAL severity is discovered in the code and adds a Trivy report as a comment to the pull request.

## Usage

```yaml
permissions:
  contents: read # for actions/checkout to fetch code
  pull-requests: write # required for adding pull request comments
…
steps:
- name: Trivy Scan and Report to PR
  uses: domstolene/trivy-pr-report@main
  with:
    github_token: ${{ github.token }}
```

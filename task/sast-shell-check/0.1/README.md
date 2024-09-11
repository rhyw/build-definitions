# sast-shell-check task

## Description:

The sast-shell-check task uses [shellcheck](https://www.shellcheck.net/) tool to perform Static Application Security Testing (SAST), a popular cloud-native application security platform.

ShellCheck is a static analysis tool, gives warnings and suggestions for bash/sh shell scripts.

## Params:

| Name              | Description                                                                                  | Default Value | Required |
|-------------------|----------------------------------------------------------------------------------------------|---------------|----------|
| KFP_GIT_URL       | Git repository to download known false positives files from.                                 | ""            | No       |
| PROJECT_NVR       | Name-Version-Release (NVR) of the scanned project, used to find path exclusions (optional).  | ""            | No       |
| RECORD_EXCLUDED   | Whether to record the excluded findings (defaults to false).<br/>If `true`, the the excluded findings will be stored in `excluded-findings.json`.  | "false"            | No       |
| CSGREP_EVENT_FILTER    | ShellCheck event filter for csgrep.  | "\[SC(1020|1035|1054|1066|1068|1073|1080|1083|1099|1113|1115|1127|1128|1143|2043|2050|2055|2057|2066|2069|2071|2077|2078|2091|2092|2157|2171|2193|2194|2195|2215|2216|2218|2224|2225|2242|2256|2258|2261)\]$"            | No       |

## Results:

| name                  | description              |
|-----------------------|--------------------------|
| TEST_OUTPUT           | Tekton task test output. |

## Source repository for image:

https://github.com/konflux-ci/konflux-test

## Additional links:

* https://www.shellcheck.net/wiki/Home
* https://github.com/koalaman/shellcheck
* https://github.com/csutils/csmock

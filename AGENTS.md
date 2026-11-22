# AGENTS.md

Write issues, pull requests, and commit messages in English.

This repository owns the PHP implementation published as `nakanoaas/uuid58`.
Run `composer validate --strict`, `composer update`, `vendor/bin/phpstan analyse`,
and `vendor/bin/phpunit`. CI covers PHP 8.1 and 8.5 without GMP or BCMath.

`tests/vectors.json` is copied from `nakanoasaservice/uuid58/spec/vectors.json`;
CI checks for drift, including weekly. Update the fixture when upstream changes.

After changing any Actions `uses:`, run `gh actions-lock` and commit the lockfile.
Releases use `vX.Y.Z` tags and the Packagist GitHub webhook. Do not push release
tags unless asked, and never move published tags.

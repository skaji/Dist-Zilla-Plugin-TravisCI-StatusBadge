# NAME

Dist::Zilla::Plugin::TravisCI::StatusBadge - Get Travis CI status badge for your markdown README

[![Build Status](https://travis-ci.org/Wu-Wu/Dist-Zilla-Plugin-TravisCI-StatusBadge.svg?branch=master)](https://travis-ci.org/Wu-Wu/Dist-Zilla-Plugin-TravisCI-StatusBadge)

# VERSION

version 0.005

# SYNOPSIS

    ; in dist.ini
    [TravisCI::StatusBadge]
    user = johndoe
    repo = p5-John-Doe-Stuff
    branch = foo        ;; "master" by default
    vector = 1          ;; SVG image

    ; or just
    [TravisCI::StatusBadge]
    ;; shortcut for "png image; master branch; user/repo from meta resources"

# DESCRIPTION

Scans dist files if a `README.md` file has found, a Travis CI `build status` badge will be added before the **VERSION** header.
Use [Dist::Zilla::Plugin::ReadmeAnyFromPod](https://metacpan.org/pod/Dist::Zilla::Plugin::ReadmeAnyFromPod) in markdown mode or any other plugin to generate README.md.

# OPTIONS

## readme

The name of file to inject build status badge. Default value is `README.md`.

## user

Github username. Might be obtained automatically (if not given) from META resources (`resources.homepage`,
`resources.repository.web`, `resources.repository.url`).

## repo

Github repository name. Might be obtained automatically (if not given) from META resources
(`resources.homepage`, `resources.repository.web`, `resources.repository.url`).

## branch

Branch name which build status should be shown. Optional. Default value is **master**.

## vector

Use vector representation (SVG) of build status image. Optional. Default value is **false** which means
using of the raster representation (PNG).

# SEE ALSO

[https://travis-ci.org](https://travis-ci.org)

[Dist::Zilla::Plugin::ReadmeAnyFromPod](https://metacpan.org/pod/Dist::Zilla::Plugin::ReadmeAnyFromPod)

[Dist::Zilla::Plugin::GithubMeta](https://metacpan.org/pod/Dist::Zilla::Plugin::GithubMeta)

[Dist::Zilla::Role::AfterBuild](https://metacpan.org/pod/Dist::Zilla::Role::AfterBuild)

[Dist::Zilla](https://metacpan.org/pod/Dist::Zilla)

# AUTHOR

Anton Gerasimov <chim@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2013 by Anton Gerasimov.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.

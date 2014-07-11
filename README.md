# NAME

Dist::Zilla::Plugin::TravisCI::StatusBadge - Get Travis CI status badge for your markdown README

[![Build Status](https://travis-ci.org/Wu-Wu/Dist-Zilla-Plugin-TravisCI-StatusBadge.png?branch=master)](https://travis-ci.org/Wu-Wu/Dist-Zilla-Plugin-TravisCI-StatusBadge)

# VERSION

version 0.004

# SYNOPSIS

    ; in dist.ini
    [TravisCI::StatusBadge]
    user = johndoe
    repo = p5-John-Doe-Stuff
    branch = foo        ;; "master" by default

# DESCRIPTION

Scans dist files if a `README.md` file has found, a Travis CI `build status` badge will be added before the **VERSION** header.
Use [Dist::Zilla::Plugin::ReadmeAnyFromPod](https://metacpan.org/pod/Dist::Zilla::Plugin::ReadmeAnyFromPod) in markdown mode or any other plugin to generate README.md.

# OPTIONS

## readme

The name of file to inject build status badge. Default value is `README.md`.

## user

Github username. Required.

## repo

Github repository name. Required.

## branch

Branch name which build status should be shown. Optional. Default value is **master**.

# SEE ALSO

[https://travis-ci.org](https://travis-ci.org)

[Dist::Zilla::Plugin::ReadmeAnyFromPod](https://metacpan.org/pod/Dist::Zilla::Plugin::ReadmeAnyFromPod)

[Dist::Zilla](https://metacpan.org/pod/Dist::Zilla)

# AUTHOR

Anton Gerasimov <chim@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2013 by Anton Gerasimov.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.

---
type: docs
bookShowToc: false
title: Introduction
---

# Introduction

This guides teaches everything you need to know to implement
any different caching strategy inside your Rails application. It assumes
you know nothing at all about caching in any of its forms. It takes from
zero to knowledge to an intermediate level in all areas. If you can't
implement caching in your app after reading this then the guide has
failed.

## Preface

This guide was originally part of my old website. I've extracted it
out to this new format so it may have an independent lifecycle and
easier maintenance. It's also an updated version of an older work with
newer sections.

I've added a totally new section on HTTP caching. Page caching is
covered briefly. HTTP caching gets much more love in this
version. I'd like to push developers towards HTTP caching as much as
possible.

Since HTTP caching was added I felt that it was only natural to cover
static assets. This aspect is usually left uncovered. Correctly handling
static assets is increasingly important as applications contain more and
more JS and CSS.

Previous sections on sweepters have been slimmed down because I don't
think they are as important.

This guide was originally written for Rails 2. Some of log examples are
extracted from Rails 2 applications. Rails 3+ does **not** output any cache
information by default. There are two ways to see what's happening in
real time.

1. Start a local memcached process with: `memached -vv` and watch
   $stdout.
2. Enable cache instrumentation and attach a log subscriber. Rails cache
   adatpers emit notifications through `ActiveSupport::Notifications`.
   These events can be logged. It's easy to attach a log subscriber. See
   the embedded gist:

<script src="https://gist.github.com/3086218.js"> </script>

I've elected to not update the log examples for Rails 3 because it does
not add any useful to the post. Following either of the methods above
will show you in real time what keys are written to cache. The only
thing that's changed is the formatting. Keep this in mind as you read
through the guide.

All that being said, please enjoy this guide to building a faster
Rails applications.

Good look out there and happy shipping!

-- [Adam Hawkins](https://slashdeploy.com), 2018

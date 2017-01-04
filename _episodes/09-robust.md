---
title: "Step 7: Make Your Software Robust"
teaching: 5
exercises: 10
questions:
- "FIXME"
objectives:
- "FIXME"
keypoints:
- "FIXME"
---

FIXME: [Taschuk's Rules](http://oicr-gsi.github.io/robust-paper/)
get you from "works on my laptop" to "runs on your cluster"

1.  Have a README that explains in a few lines what the software does and what its dependencies are
1.  Print usage information when launching from the command line that explains the software's features
1.  Give the software a meaningful version number
1.  Make older versions available
1.  Reuse software (within reason)
1.  Do not require root or other special privileges
1.  Eliminate hard-coded paths
1.  Allow configuration of all useful parameters from the command line
1.  Include a small test set that can be run to ensure the software is actually working
1.  Produce identical results when given identical inputs

FIXME: Assume your users are following [Noble's rules][noble-rules]

1.  Put each project in its own directory which is named after the project
1.  Put text documents in `doc/`
1.  Put raw data and metadata in `data/`
    *   Treat as read-only thereafter
1.  Put files generated during analysis in `results/`
    *   Preliminary cleanup is part of the analysis
1.  Put project source code in `src/`
1.  Put external scripts and compiled programs in `bin/`
    *   Unless they are system-installed
1.  Name all files to reflect their content or function

{% include links.md %}

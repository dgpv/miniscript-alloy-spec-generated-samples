# The samples generated with https://github.com/dgpv/miniscript-alloy-spec

The `8ed9d5a6d084d70e607eb4fb8801ba86d481eb6c.zip` file contains 5896
.dot files that are a result of running gui automation on Alloy analyzer
on Miniscript formal spec from https://github.com/dgpv/miniscript-alloy-spec,
at commit 8ed9d5a6d084d70e607eb4fb8801ba86d481eb6c, with "main" run clause

The `33b85f29d53e2623b955d55afe9061f5d0fc96d3_malleable.zip` file contains
7024 .dot files that are a result of running the same automation
at commit 33b85f29d53e2623b955d55afe9061f5d0fc96d3 with "main" run clause,
but with `main_search_predicate` modified to say `RootNode not in NonMalleableHolds`.
This means that all samples represent scripts that do not have non-malleable
property.

The `8f1e80d95c49d49563b97fb97fd3ed38b55b4672_incorrect.zip` file contains
5574 .dot files that are a result of running the same automation
at commit 8f1e80d95c49d49563b97fb97fd3ed38b55b4672 with "main" run clause,
but with `main_search_predicate` modified to say `not correctness_holds_for_all_nodes`.
This means that all samples represent scripts that are not correct.

The `8f1e80d95c49d49563b97fb97fd3ed38b55b4672_timelock_conflicts.zip` file contains
1773 .dot files that are a result of running the same automation
at commit 8f1e80d95c49d49563b97fb97fd3ed38b55b4672 with "main" run clause,
but with `main_search_predicate` modified to say `tl_conflict in timelocks[RootNode]`.
This means that all samples represent scripts that contain a timelock conflict.

These dot files can be processed by the `tools/parse_miniscript_dot.py`
script in the aforementioned miniscript-alloy-spec repository.

For some reason, some of Miniscript fragments can be found more often
in the samples (Multi is almost always present, for some reason), while
other fragments are more rare (Thresh is found rarely). But there's still
multiple instances with each Miniscript fragment.

The .dot files contain information about witnesses, too. The parser script
may generate the output that ignores witnesses, and then there will be fewer
unique instances. But for completeness, all of the files are present here,
in case someone would find it useful to analyse witness information.

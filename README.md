# The samples generated with https://github.com/dgpv/miniscript-alloy-spec

The 8ed9d5a6d084d70e607eb4fb8801ba86d481eb6c.zip file contains 5896
.dot files that are a result of running gui automation on Ally analyzer
on Miniscript formal spec from https://github.com/dgpv/miniscript-alloy-spec,
at commit 8ed9d5a6d084d70e607eb4fb8801ba86d481eb6c

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

Assign names to the rewrite rules in the semantics of the K framework and document the applied rewrite rules in Markdown

## Usage


```bash
python kompile_wrappter.py {semantics_file}
bundle install
ruby KToMD.rb {script_file} {semantics_file} --join
```

e.g

```md
// imp.md
rule [assign]: <k> X = I:Int; => .K ...</k>
<state>... X |-> (_ => I) ...</state> // [assign] is important
```

```bash
python kompile_wrapper.py imp.md

bundle install
ruby KToMD.rb sum.imp imp.md --join
```

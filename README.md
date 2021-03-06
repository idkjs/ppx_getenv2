See http://rgrinberg.com/posts/extension-points-3-years-later/

# Test

```sh
> ➜ dune runtest
Done: 0/0 (jobs: 0)File "test/pp.expected", line 1, characters 0-0:
         git (internal) (exit 1)
(cd _build/default && /usr/local/bin/git --no-pager diff --no-index --color=always -u test/pp.expected test/pp.result)
diff --git a/test/pp.expected b/test/pp.result
index 8192914daef0..2403759cc625 100644
--- a/test/pp.expected
+++ b/test/pp.result
@@ -2,3 +2,4 @@ let () =
   match ((Some ("foobar"))[@explicit_arity ]) with
   | None -> ()
   | Some _ -> ()
+let () = assert (None = None)
```

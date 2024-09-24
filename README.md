# Bash Commands

Useful bash commands

* `sudo lsof -i -P -n | grep LISTEN` - checks ports listening
* `open -a Google\ Chrome\ Canary --args --disable-web-security --user-data-dir=$HOME/profile-folder-name` - Opens Canary with web Security disabled. Helpful to test CORS.
* Split file in chunks, rename them, unzip them

```cmd
 split -n 50 -d quicksightEntities.jsonl quicksightEntities_
 for i in {0..9}; do mv quicksightEntities_0$i quicksightEntities_$i.jsonl; done
 for i in {10..49}; do mv quicksightEntities_$i quicksightEntities_$i.jsonl; done
 for i in {0..49}; do mv quicksightEntities_$i.jsonl ../cell-$i/; done
 for i in {0..49}; gunzip asr-full_$i.jsonl.gz; gunzip smlgsLineItems_$i.jsonl.gz; done
 for i in {0..49}; gunzip asr-full_$i.jsonl.gz && gunzip smlgsLineItems_$i.jsonl.gz; done
 for i in {0..49}; gunzip asr-full_$i.jsonl.gz; done
 for i in {0..49}; do gunzip asr-full_$i.jsonl.gz && gunzip smlgsLineItems_$i.jsonl.gz; done
```

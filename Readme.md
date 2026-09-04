# CPOLD the dumbest versioning system ever

Did you ever issued a command like this one ?
```
cp myfile myfile.old
```

Never make such complicated thing again and use cpold instead
```
cpold myfile
```

don't worry if there's already a *myfile.old* file it will be **cpold** itself to *myfile.old.old* and so on

And yes it works with folders too, so you can do
```
cpold myfolder
```

## 2026 addition (yes this project is still alive)
made a mistake and want your file back the way it was ? get **unold**, just point at the backup you want, *.old*'s included:
```
cpold --unold myfile.old
```
this brings *myfile.old* back onto *myfile*, backups left untouched

need an older generation ? spell it out, it's dumb but explicit:
```
cpold --unold myfile.old.old.old
```
this brings *myfile.old.old.old* back onto *myfile*

since restoring overwrites *myfile* you'll be asked to confirm each time, skip that with `-f`/`--force` (handy in scripts):
```
cpold --unold -f myfile.old
```

forgot everything already ? `cpold -h` / `cpold --help` (or just `cpold` with nothing after it) prints a reminder

and for sure this is public domain :)

# Studio and/or workspace is not starting

If developer studio and/or workspace is not start after a crash etc. you can try following steps to resolve it. Start from first one and if it does not help, proceed to next one:

1. Try to start studio with _clean_ option. 

```
C:\Progress\OpenEdge\oeide\eclipse\eclipse.exe -clean  -vm "C:\Progress\OpenEdge\jre\bin\javaw.exe"
```
Depending on where your installation is.

2. Remove *.snap* file from your workspace

.snap file is located in
```
${workspace}\.metadata\.plugins\org.eclipse.core.resources 
```
This has helped me many times, when workspace has been locked (not opened at all).

3. Start Studio with _clearPersistedState_ option

```
C:\Progress\OpenEdge\oeide\eclipse\eclipse.exe -clearPersistedState  -vm "C:\Progress\OpenEdge\jre\bin\javaw.exe"
```
Note: this restores all perspectives to initial state, closes all previously opened files, closes scrath pad etc. 

Alternative to this is to delete folder _${workspace}\.metadata\.plugins\org.eclipse.e4.workbench_



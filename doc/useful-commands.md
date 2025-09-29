# Namespace stuck in "Terminating" Status

```posh
$ns = "my-stuck-namespace"

$nsObj = kubectl get namespace $ns -o json | ConvertFrom-Json

if ($nsObj.spec) { $nsObj.spec.finalizers = @() }
if ($nsObj.metadata -and $nsObj.metadata.finalizers) { $nsObj.metadata.finalizers = @() }
```
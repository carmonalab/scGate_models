# Cell type gating models for scGate

Models can be loaded into scGate using the syntax:
```r
models.db <- get_scGateDB()
model.Tcell <- models.db$human$generic$Tcell

gated <- scGate(obj, model=model.Tcell)
```

To use scGate as a multi-classifier, load one of the collections from the DB:
```r
models.db <- get_scGateDB()
models.TME <- models.db$human$TME_HiRes

gated <- scGate(obj, model=models.TME)
table(gated$scGate_multi)
```

Note: we will tag versions of this DB using the format 'vN.M' (e.g. v1.4). This format is understood by scGate to download specific versions of the DB

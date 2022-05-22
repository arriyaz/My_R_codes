## Check the index/number of a column in a dataframe

```R
which(colnames(df)=="columnName" )
```
## Save a plot as svg image in R
```R
svglite("path/plot_name.svg",
        width =3,
        height =3)
#plot
plot_object

dev.off()
```
## Save a plot as png image in R

```R
png("path/plot_name.png",
        width=3000,
        height =3000,
        res=600)
#plot
plot_object

dev.off()
```

## To save all objects in a R script

```R
save.image("Some_Name.RData")
```

## To load all objects in a R script
```R
laod("Some_Name.RData")
```



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
-------
## To make the texts editable in svg file from svglite() R function
First run the follwoing code on the desired svg file, then open the file in **Inkscape**. Then you will find the all text can be edited.
Run the following code in bash terminal

```bash
sed -i "s/ textLength='[^']*'//" file.svg
```
-------

### Save a plot as png image in R

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
load("Some_Name.RData")
```



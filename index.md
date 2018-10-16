## BITACORA R

Codigo de R [Hell](https://jushua.github.io/).


### Librería R para Geolocalización

Leaflet

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

```markdown
`
# install.packages("leaflet")
library(leaflet)

# cargamos data
df= read.csv(file = "C:/Users/B32652/Desktop/trash/coordenadas4.txt",sep = ",")
 
data = df
data = subset(df,mes == "201807")

# generamos mapa
# proveedor Stamen.TonerLite, OpenStreetMap.HOT, ... http://leaflet-extras.github.io/leaflet-providers/preview/
m <- leaflet(data) %>% addProviderTiles(providers$OpenStreetMap.HOT) 
m  = m %>%   addPolylines(lng = ~lon, lat = ~lat, color = "blue")
m  = m %>%   addCircles(lng = ~lon, lat = ~lat, color = "red", radius = 50)
m

m <- leaflet(data) %>% addProviderTiles(providers$OpenStreetMap.HOT) 
m  = m %>%   addCircles(lng = ~lon, lat = ~lat)
m

# agregar leyenda
m  = m %>%  addLegend("bottomright", colors = c("green","yellow","red","black","black"), labels = c(5:1),title = "NSE",opacity = 1)
`
```





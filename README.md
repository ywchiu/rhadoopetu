# RHadoop 課程 @etu
### Slides
https://www.slideshare.net/secret/4e7Cw8FzAb22K


### 操作說明影片
- https://youtu.be/vLPlI3MdCv8

- https://youtu.be/5-oPDfy1LxY

- https://youtu.be/dUeLbl1dcXs

### Source Code
http://rpubs.com/ywchiu/25570


### 2330 Analysis
tw2330 = read.csv("~/Downloads/tw2330.csv", head=TRUE)

head(tw2330)

head(tw2330,10)

tail(tw2330,10)

str(tw2330)

tw2330$Date = as.Date(tw2330$Date)

str(tw2330)

tw2330[tw2330$Date >='2014-03-01' & tw2330$Date < '2014-09-01' ,]

tw2330_mar_sep = tw2330[tw2330$Date >='2014-03-01' & tw2330$Date < '2014-09-01' ,]

min(tw2330_mar_sep$Close)

max(tw2330_mar_sep$Close)

mean(tw2330_mar_sep$Close)

hist(tw2330_mar_sep$Close)

hist(tw2330$Close)

boxplot(tw2330$Close)

head(tw2330[order(tw2330$Close, decreasing=TRUE) ,])

tw2330$tf = ifelse(tw2330$Close - tw2330$Open > 0 , TRUE, FALSE)

table(tw2330$tf)

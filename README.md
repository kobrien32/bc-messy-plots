# bc-messy-plots
Messing around with R code for bear creek lake data.

> BC.data <- read.csv("C:/Users/Keenan/Desktop/Bear Creek/removenas.csv", header = T)

> plot(x = BC.data$monthyear, y = BC.data$E.coli_CFUper100ml)

> plot(x = BC.data$site, y = BC.data$E.coli_CFUper100ml)

> plot(x = BC.data$site, y = BC.data$monthyear)

> plot(x = BC.data$monthyear, y = BC.data$site)

> site.means <- aggregate(BC.data, list(BC.data$monthyear), FUN = "mean")

> plot(x = site.means$Group.1, y = site.means$E.coli_CFUper100ml)

> qapp.means <- aggregate(BC.data, list(BC.data$EPA), FUN = "mean")

> month.means <- aggregate(BC.data, list(BC.data$month), FUN = "mean")

> plot(x = month.means$Group.1, y = month.means$E.coli_CFUper100ml, pch = 19)

> year.means <- aggregate(BC.data, list(BC.data$year), FUN = "mean")

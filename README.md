library(readxl)
guitite <- read_excel("C:/Users/shaun/Downloads/Datos_proyecto_eco (1).xlsx", na = c("", "NA"))
View(guitite)
#-----------------ANOVA DE DOS VIAS------------------
modeloG <- aov(Numero_agallas ~ Zona * Tamano_hoja, data = guitite) # Dan significativas todas, hasta la interaccion
summary(modeloG)
TukeyHSD(modeloG)

Hola

# data_bank

require(pracma)
datas<-read.csv(file = "./UFMG/Arquivos/RStudio/Biometria.txt",sep = "/")
head(datas,n = 7)

names(datas) <- c("Codigo","Nome.cientifico","Sexo","CP_m","CT_m","Peso_g","Campanha")

print(mean(datas$Peso_g))
print(sd(datas$CP_m))
plot(datas$Peso_g)

for(v in 1:length(datas$Sexo)) {
  if (datas$Sexo[v] =="F"){
    datas$Sexo[v] <- "Femea"
  } else {
    datas$Sexo[v] <- "Macho"
  }
}
print(datas)

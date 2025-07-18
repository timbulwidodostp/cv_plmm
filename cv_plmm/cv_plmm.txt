# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Fit penalized linear mixed models to correct for unobserved confounding effects Use plmm and cv_plmm With (In) R Software
install.packages("plmmr")
library("plmmr")
cv_plmm = read.csv("https://raw.githubusercontent.com/timbulwidodostp/cv_plmm/main/cv_plmm/cv_plmm.csv",sep = ";")
# Estimation Fit penalized linear mixed models to correct for unobserved confounding effects Use plmm and cv_plmm With (In) R Software
X <- cbind(cv_plmm$X1, cv_plmm$X2, cv_plmm$X3)
y <- cv_plmm$y
par(mfrow = c(1, 2))
plmm <- plmm(X, y) 
plmm_ <- summary(plmm, idx = 50)
print(plmm_)
plot(plmm)
cv_plmm <- cv_plmm(X, y)
plot(cv_plmm)
summary(cv_plmm)
# Fit penalized linear mixed models to correct for unobserved confounding effects Use plmm and cv_plmm With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
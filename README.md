# Programming-Assignment-2-Lexical-Scoping
Caching the Mean of a Vector and the Inverse of a Matrix
#This function is useful to calculate the absolute mean error, where
#x (actual value), y (forecast)
#with this value we can determine the validity of a regression model
rmsolve <- function(x,y){
  T<-abs(((x-y)/x)*100)
  mean(T)
} 

g <- rmsolve(x,y)


data<-matrix(c(1,0,0,0,0,0,1,0,0,0,-1,0,1,0,0,0,0,0,1,0,0,0,0,0,1),
             nrow=5,byrow=T)
# Solve is a simple function to calculate the inverse of a matrix
lod<- function(x=matrix()){
  
  solve(x)
}
#Inverse matrix
m <- lod(matrix(data,5,5))

#2
lod2<- function(x=matrix()){
  #the number of rows must be added to obtain the identity matrix, in this case it is 5 
  I <- diag(1,nrow=5)
  solve(x,I)
}
#Inverse matrix
m2 <- lod2(matrix(data,5,5))

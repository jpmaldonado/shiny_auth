library(shiny)
library(shinydashboard)
library(dashboardthemes)
library(tidyverse)
library(digest)
library(shinyjs)
library(DT)
library(glue)

source("auth_module.R")
source("pwc.R")

user_base <- tibble::tibble(
    user = c("admin", "user"),
    password = c("admin_pass", "user_pass"), 
    permissions = c("admin", "standard")
)



###############################################################################
##
##  Change the flag to avoid having to authenticate during development
##
###############################################################################

DEVELOPMENT <- T

PERMISSION <- NULL
USER_AUTH <-  F

if(DEVELOPMENT){
  PERMISSION <- "admin"
  USER_AUTH <-  T
}

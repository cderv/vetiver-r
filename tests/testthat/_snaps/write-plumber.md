# create plumber.R with packages

    Code
      cat(readr::read_lines(tmp), sep = "\n")
    Output
      # Generated by the vetiver package; edit with care
      
      library(pins)
      library(plumber)
      library(vetiver)
      library(rapidoc)
      
      # Packages needed to generate model predictions
      if (FALSE) {
          library(beepr)
          library(janeaustenr)
      }
      b <- board_folder(path = "/tmp/test")
      m <- vetiver_pin_read(b, "cars1")
      
      #* @plumber
      function(pr) {
          pr %>% vetiver_pr_predict(m)
      }

# create plumber.R with no packages

    Code
      cat(readr::read_lines(tmp), sep = "\n")
    Output
      # Generated by the vetiver package; edit with care
      
      library(pins)
      library(plumber)
      library(vetiver)
      b <- board_folder(path = "/tmp/test")
      m <- vetiver_pin_read(b, "cars1")
      
      #* @plumber
      function(pr) {
          pr %>% vetiver_pr_predict(m)
      }

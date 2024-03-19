# trace_classifier_with_adding
An addition to the official code includes an extension to the existing detail and a reference to the original code https://github.com/shashadehuajiang/trace_classifier 

adding lag to the orginal code 
change file config.py add size_lag with lag=0 Unchanged state
and lag>0 Adds more columns to the base vector as the number of lags given
where each column brings the distance in time between it and n-i
where i represents the number of the added column and runs from 0 to n-1

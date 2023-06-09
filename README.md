### ACCURACY with best values for number of hidden layers, neurons in hidden layer

* epocs = 200, batch size = 10, train images = 6000, test images = 10000, hidden layers = 1, neurons in hidden layer = 20
  * ACC: 91.1 %

* epocs = 200, batch size = 100, train images = 60000, test images = 10000, hidden layers = 1, neurons in hidden layer = 20 
  * ACC: 93.3 %


### Serial vs OPENP TIME TAKEN

* SERIAL: epocs = 200, batch size = 10, train images = 6000, test images = 10000, hidden layers = 1, neurons in hidden layer = 20
    * TIME: 166.8 (s)

* OMP: epocs = 200, batch size = 10, train images = 6000, test images = 10000, hidden layers = 1, neurons in hidden layer = 20
  * TIME: 33.32 (s)
  * batch size = num of threads for the loop that goes over m images

* SPEEDUP = 5.2 times


### COMPILING AND RUN

* serial: 
  * ```make test_nn```
  * ``` ./test_nn <num_hidden_layers> <neurons_in_each_hidden_layer> <num_of_epocs> <batch_size>```

* omp:
  * ```make test_nn_omp```
  * ```./test_nn_omp <num_hidden_layers> <neurons_in_each_hidden_layer> <num_of_epocs> <batch_size>```
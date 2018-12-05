# sigpool
This package implements monitoring the signals sent to the process and setting a flag after a certain time.
To monitor the a signal you can say for example `sigpool.watch('SIGUSR2')` and then test in your code if the signal has been sent to your process by `if 'SIGUSR2' in sigpool.flags: ....`. You may also set a timer that raises a flag after t seconds
by `sigpool.wait_n_raise(t)`. There is a helper function `sigpool.str2time(s)` that helps one turn strings like "3h 4s" into seconds.

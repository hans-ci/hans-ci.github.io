### Welcome to automated testing!
Dronetest is a set of Ruby scripts which executes per-commit and per-PR tests on real autopilot hardware. Its uses [Hans-CI](http://github.com/hanssaurer/px4test) to apply teutonic thoroughness. In addition, it supports long-term soak tests on selected branches (e.g. stable or master). It supports Mac OS and tiny Linux computers such as the [Intel Compute Stick](http://www.intel.com/content/www/us/en/compute-stick/intel-compute-stick.html). After installing the prerequisites according to the [README.md](https://github.com/hanssaurer/px4test/tree/master/README.md), the test setup is quickly installed:

```
$ git clone https://github.com/hanssaurer/px4test.git
$ cd px4test
$ # Create the config.txt according to the README.md instructions
$ ./run.sh # For a quick test
$ # Or add watchdog.sh as a cron-job entry which will auto-update the script.
```

### Testing Output
The system generates a HTML report available for download and sends a summary via email. The report includes the console output of the autopilot and a GIF showing the led pattern.

### TODO

  * Stack dump / crash detection
  * GDB / JTAG readout, parsing and reporting
  * Runtime statistics for specific branches / commits to help bisection a bit (correlation assumptions..)

### Authors and Contact
Hans Saurer (@hanssaurer), Lorenz Meier (@LorenzMeier).

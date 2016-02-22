# ansi-tmp
tmp repo to test new vagrant feature improving usability under Windows hosts...

## requires

* virtual box
* vagrant > 1.7.x

## directions

* clone the repository as usual to your Windows host
* from the terminal, change directory into the repository folder (`cd /path/to/repo`)
* execute `vagrant up`

The build should complete without error. The build script is intentionally trivial, as its main purpose is to demonstrate new Vagrant compatibility on Windows hosts. 
Once the build completes, the guest OS should have the program `htop` installed:

* log into the guest vm as usual with `vagrant ssh`
* check for the presence of htop: execute `htop` at the commandline
* assuming that htop loads (list of all running processes), we have success.
* type `q` to exit htop
* `ctrl-D` to exit the vm
* use `vagrant destroy` to get rid of the vm (some Windows terminal emulators seem to require the `--force` option: `vagrant destroy --force`).
* you can now safely delete the repository

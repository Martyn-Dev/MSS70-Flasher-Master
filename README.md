Please don't judge my code, I'm really not a programmer by trade, everything I have managed to achieve is self taught trial and error :)

# MSS70 Flasher for the Z4M
Tool to read the MSS70 DME. The end goal will be to prove write facilities too but at the moment that is out of my reach.


### Prerequisites
This application uses .Net Framework 4.5.2

Any INPA-compatible OBDII cable should work with this application. Make sure your cable latency is set to 1ms

You will need EdiabasLib.dll to compile and run this application.
The application assumes you have an ediabas installation in the default directory along with E46, E60, E65, E83, or E85 daten files.
If you don't have / want Ediabas installed, you will need to find a copy of MSS70.prg and set the .config file to reflect the directory and filename of those files.


### Usage
Change the settings as necessary in the 'MSS70 Flasher.exe.config' file. 
Default port is COM1, default sgbd directory is C:\Ediabas\ECU, and default sgbd is D_Motor.GRP (should automatically resolve to MSS70.prg if connected to an MSS70 DME)


##### Identify your DME
Start the application, connect your interface to your OBDII port, and click "Ident DME"
If successful, the application should autopopulate some information from your DME

##### Reading your DME
For the tune, simply click "Read DME". 

You will be prompted whether you wish to take a full read or a partial read. 

The full read is a full backup of your flash, this contains the program and parameter space and takes around 50 minutes to complete.

The partial read is just the parameter space and takes around 3 mins to complete.

Save the file(s) whereever you like

## Built using

* [EdiabasLib](https://github.com/uholeschak/ediabaslib) - Used to communicate with the DME

## Acknowledgments

* The MSS70 Flsaher is a fork of Terraphantm's fantastic MS45-Flasher, I have merely modified it to work with the MSS70.

If this application has been useful for you and you would like to go a bit further with tuning, please consider checking out [bimmerlabs](https://www.bimmerlabs.com). The site is still growing, but our goal is to allow full control of most BMW DMEs. 

## License

This project is licensed under The GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details

## Disclaimer: 
This program is inherently invasive, and can render your DME unbootable and your car undriveable. Care must be taken when using this application. In no respect shall the authors or contributors incur any liability for any damages, including, but limited to, direct, indirect, special, or consequential damages arising out of, resulting from, or any way connected to the use of the application, whether or not based upon warranty, contract, tort, or otherwise; whether or not injury was sustained by persons or property or otherwise; and whether or not loss was sustained from, or arose out of, the results of, the item, or any services that may be provided by the authors and contributors.

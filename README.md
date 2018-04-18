# Ciclopi Case Study

**Ciclopi** (www.ciclopi.eu) is a bike sharing service that is operating in Pisa since 2013. It is a station-based service: a registered user may pick up a bike from one of the stations in the town and can drop it in another station.

The company running the service has provided us a dataset with the logs of all the operations on the system during 2015. An __operation__ is a digital trace containing the description of a pick of a bike from a dock in a station, the duration of the renting, and the drop off at the dock of the destination station. All these data are provided as a single table with multiple attributes (in italian):
 * Comune: The municipality where the station is located (in our case is Pisa)
 * Prelievo (Pick up):
     * StazPrelievo: The station where the bike is picked up
     * DataOraPrelievo: The timestamp when the bike was taken
     * ColonninaPrelievo: The dock within the station where the bike was taken
 * Deposito (drop off):
     * StazDeposito: The station where the bike is dropped
     * DataOraDeposito: The timestamp when the bike was dropped
     * ColonninaDeposito: The dock within the station where the bike was dropped
 * IDBadge: anonymized identification of the user taking the bike
 * NumeroBadge: anonymized identification of the user taking the bike
 
 
 ## Analytical Environment - Installation and Setup
 We are going to analyze these data using the Python environment and the Jupyter Notebook for managing the data.
 As a reference, we assume there is the Anaconda environment already installed.
 To be sure to have all the requirements aligned for the developing, we will create an Anaconda Environment dedicated for this task
```
$> conda create -n dvva python=3.6 anaconda -y
```

where //dvva// is a mnemonic name assigned to the new environment.
Then we will activate the new created environment:

```
$> source activate dvva
```

and we will install the required packages:
```
conda install plotly=2.5.1  pandas=0.22.0 xlrd=1.1.0  geopandas=0.3.0 
```

The libraries we are installing are:
 * **plotly**: the library used to create charts
 * **pandas**" a library to manage tabular data
 * **xlrd**: a library to read and parse Excel files
 * **geopandas**: extension of the pandas library to handle geometric and geographic data

We are also installing a library to manage and create color palettes:
```
pip install colorlover
```

The previous step is done once for the working computer.
For successive sessions of work, we will only activate the environment:
```
$> source activate dvva
```

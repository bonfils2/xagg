# XAGG

XML Aggregator for CMIPx data

Dependencies:
```
python3, joblib, scandir, cdscan (part of cdms2)
```

Setup:
----------------
* Create anaconda environment with dependencies (creates a Py3 environment by default)
```
conda create -n xagg -c conda-forge -c cdat cdms2 joblib scandir
```

* Download local tables database
```
cd tools
./updateTables.sh
cd ..
```

Run software:
----------------
* Execute test cases
```
./xagg.py -f mon -v tas --outputDirectory ~/tmp > log.txt
```
Or
```
./xagg.py -f mon -v tas -e hist-CO2 --outputDirectory ~/tmp --updatePaths False > log.txt
```

* Execute complete scan
```
./xagg.py --outputDirectory ~/tmp > log.txt
```
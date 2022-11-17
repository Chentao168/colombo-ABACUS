# ABACUS Hands-On ABC

## A. SCF

### A.1 Download input files
```
>> cd /data
>> git clone https://gitee.com/deepmodeling/colombo-academy-tutorials.git -b develop
>> cd colombo-academy-tutorials
>> cd ABACUS/
>> cd MgO_LCAO
>> ls
   band_structure  optimization  SCF
```

### A.2 Run SCF
```
>> cd SCF
>> abacus
```

### A.3 Get ETOT
```
>> cd OUT.MgO
>> grep ETOT running_scf.log
```

## B. Optimization

### B.1 Run optimization
```
>> cd ../../optimization
>> abacus
```

### B.2 Check optimized structure
```
>> cd OUT.MgO
>> ls
   .cif file
```

## C. Band Structure

### C.1 Run SCF
```
>> cd ../../band_structure
>> cp INPUT_scf INPUT
>> cp KPT_scf KPT
>> abacus
```

### C.2 Run NSCF
```
>> cp INPUT_nscf INPUT
>> cp KPT_nscf KPT
>> abacus
```

### C.3 Install `abacus-plot`
```
>> cd ~/abacus-develop/tools/plot-tools
>> pip install lxml
>> python3 setup.py install
```

### C.4 Plot band structure
```
>> cd /data/colombo-academy-tutorials/ABACUS/MgO_LCAO/band_structure/OUT.MgO/
>> cp ../KPT ./
>> cp ../config.json ./
>> abacus-plot -b
```

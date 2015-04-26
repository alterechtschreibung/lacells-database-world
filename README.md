lacells-database-world
======================

A cell tower database for µg UnifiedNlp (UnifiedNlp) with LocalGsmNlpBackend, including woldwide tower information from OpenCellId and Mozilla Location Services. cell tower database for µg UnifiedNlp (UnifiedNlp)

About µg UnifiedNlp:
µg UnifiedNlp is a FLOSS (Free/Libre Open Source Software) tool for geolocating android phones without Google's Geolocation service. It allows apps that use Android's coarse or network locating features to geolocate the phone which is usually faster and less battery consuming then GPS. 
The real location work is done by backends (plug-ins) that can be configured through the UnifiedNlp UI. 
The LocalGsmNlpBackend backend performs no network data. All data acquired by the phone stays on the phone and no queries are made to a centralized AP location provider.
Therefor a database must be placed in the .nogapps folder of your internal phone storage.

About this database:
This database was generated with https://github.com/alterechtschreibung/lacells-creator-mod 
The database is required for the LocalGsmNlpBackend and includes woldwide tower information from OpenCellId and Mozilla Location Services.

Folder for the generated database: 
/storage/emulated/0/.nogapps/lacells.db

Downloads besides this database:
https://f-droid.org/repository/browse/?fdid=com.google.android.gms

https://f-droid.org/repository/browse/?fdid=org.fitchfamily.android.gsmlocation

µg UnifiedNlp is part of the μg Project at https://github.com/microg 

License:
http://creativecommons.org/licenses/by-sa/3.0/legalcode

### How To Use
1. Download and extract the lacells.tar.xz
2. Push the the generated database to /storage/emulated/0/.nogapps/lacells.db
```
	adb push lacells.db /storage/emulated/0/.nogapps/lacells.db
```

### Comment on database sizes (20Dec2014)
The database has a significant size.

Reasons:

The 95,171,584 byte cells-world.db contains 2,486,708 cell towers. As of 20Dec2014, a database from OpenCellId for the whole world will contain 6,891,208 towers (177% increase in tower count).

To the second point, adding Mozilla data increases the non-duplicate tower count to 8,456,327 a total 240% greater than the original database.

To the last point, adding indices for faster run time access increase the non-duplicate combined database from 423,677,952 to 729,165,824 bytes (72% increase).


django-dumpdata-chunks
======================

Script is a fork of django's dumpdata, but dumps data in chunks to avoid MemoryError

Django-dumpdata-chunks is `BSD licensed` ( http://www.linfo.org/bsdlicense.html ).

Please let me know if you have any questions.

Example usage:

1) Dump data into many files:

mkdir some-folder

./manage.py dumpdata_chunks your-app-name --output-folder=./some-folder --max-records-per-chunk=100000

2) Load data from the folder:

find ./some-folder | egrep -o "([0-9]+_[0-9]+)" | xargs ./manage.py loaddata

NOTE: you can also generate a script to load data:

find ./some-folder | egrep -o "([0-9]+_[0-9]+)" |sort | awk '{print "./manage.py loaddata "$1}' > script-to-loaddata.sh

GENERAL LINKS:

`Django`: http://djangoproject.com/

`Django Code of Conduct`: https://www.djangoproject.com/conduct/

`BSD licensed`: http://www.linfo.org/bsdlicense.html
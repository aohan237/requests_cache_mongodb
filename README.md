# requests_cache_mongodb
just make mongodb to cache request

for distrabute requests  cache usage.

if you want to make requests cache,you may want the requests_cache which is  far far better than this project

usage:

from requests_cache_mongodb.cache import cache_session
mongo_uri="mongodb://"
my_session=cache_session(mongo_uri,dbname='tmp', colname='cache', expire_time=None, disabled=False)
#only mongo_uri is required,expire_time you need to supply int,and disabled need to supply Boolen

a=my_session.get('http://www.google.com/')
if you set expire_time,the url cache will be only stored in the expire_time.
if you set disabled is  True,no cache  will be avaiable.

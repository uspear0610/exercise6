import json
import requests

url_local ="http://127.0.0.1:4242/api/put"

def insert(metric_name, ID , value):
    data={
        "metric":metric_name,
        "timestamp":time.time(),
        "value":value,
        "tags":{
            "ID":ID
        }
    }
    ret = requests.post(url_local, data=json.dumps(data))
    time.sleep(1)

if type == "0070" : # TH
                #print s
                print "battery : " , bigEndian(batt)
                temperature = bigEndian( s[64:68] )
                v1 = -39.6 + 0.01 * temperature

                t = int(time.time())
                print "temperature %d %.2f nodeid=%d" % ( t, v1, bigEndian( nodeID ) )                    insert("temperature",nodeID,v1)

        else:
                #print >> sys.stderr, "Invalid type : " + type
                pass

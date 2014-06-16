SOSGui
======
Partially funded by NASA grant.  Initially developed at Denver Museum of Nature & Science (DMNS) with work provided by independant contractor Andrew Strickland as an open-source project for the SOS community.  DMNS does not provide any support for this product and encourages community development to grow its capabilities as Science on a Sphere evolves.

Technologies used - see list-o-tech.md

Installation dependencies:
- must have Node 10 with NPM (see http://nodejs.org/download/)
- once this is cloned to SOS computer (as SOS user), go into science-on-sphere directory and run: npm install
- create in science-on-sphere directory a config.json file using the following as an example:
 {
        "sosTelnet":{
            "host": "127.0.0.1",
            "port": 2468
        },
        "controlInterface":{
            "server":{
                "port": 3500
            }
        },
        "cmsInterface":{
            "server":{
                "bind": "0.0.0.0",
                "port": 3510
            },
            "library": [
                "/shared/sos/media",
                "/shared/sos/rt",
                "/home/sosdemo/sosrc"
            ],
            "playlistFsLocation": "/ml-sos-cms-data/playlists"
        },
        "database":{
            "fsLocation": "/ml-sos-cms-data/database"
        }
    }

NOTE: 
- "library" locations can be modified if playlist.sos files are stored elsewhere
- "playlistFsLocation" location can be different.  You should manually make this directory location.
- "fsLocation" location can be different.  You should manually make this directory location.
- 

After that run:

    node index.js
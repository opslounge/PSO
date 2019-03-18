# PSO VOLUME creation guide


CREATING VOLUMES
-------------------------------------------------------
####Create a new volume using a label as defined in your "pure.json" (labels are key value pairs)
docker volume create --driver pure -o size=100gb snaptest --label=1b

####Create a new volume with PSO###
docker volume create --driver pure -o size=100GB  snaptest



REMOVING VOLUMES
-------------------------------------------------------
####Remove a volume#### 
docker volume rm --driver pure -o size=1GB andyparsonsiscsidockertestvolume



SNAPSHOTS
-------------------------------------------------------
####Create a brand-new volume of that size, could be on any array managed by PSO.
`-o volume_label_selector=<xxx>`

####Create a copy of a source volume. Snap a volume
docker volume create --driver pure -o source=<volumename> : Create a copy of this volume, obviously the copy is created on the same array. <source> can be a volume or a snapshot. 

####Create a copy of an existing volume####
docker volume create --driver pure -o import_from_src=<volumename>




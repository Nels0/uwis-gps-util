take raw gps data
 - select which diver unit
 - import the log
 - get a log for time/gps/depth
 - store as... dict?

get time intervals from photo exifs
 - store as... tuple?

filter gps log by time

Filter bad GPS points
 - automatic error rejection?
    -  distance from 4 point average?
    - some statistics thing?
    - catch next point based on depth error?
 - Manual error rejection?
        - export to .kml?
        - visualise on a GUI?
    - manually get list of points to reject
    - delete points from list 
        - by index?
        - by GUI/checklist?

Create gps data that matches exif timestsamps
 - linear interpolation?
 - doing anything more complex probably not worth it.


Steps:
Terminal application, with command line arguments.

Stage 1: check (check flag)
 - read GPS data into dict
 - read exif data (as list)
 - export to klm 
Stage 2: run (manual filtering flag)
 - read GPS data into dict
 - read exif time data (as list)
 - Remove given points from list (cmd or text file?)
 - interpolate for every exif timestamp
 - output GPS log to file OR append to EXIF data of photos (another flag?)
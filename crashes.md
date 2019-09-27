

```python
import pandas
csv = pandas.read_csv("crashes.csv")
```


```python
list(csv.columns)
```




    ['Date Time',
     'Day of Week',
     'Object 1',
     'Object 2',
     'Street Number',
     'Street Name',
     'Cross Street',
     'Near Street',
     'Location',
     'May involve cyclist',
     'May Involve Pedestrian',
     'Manner of Collision',
     'First Harmful Event Location',
     'First Harmful Event',
     'Ambient Light',
     'Weather Condition 1',
     'Weather Condition 2',
     'Traffic Control Device Type',
     'Traffic Control Device Functionality',
     'Road Surface Condition',
     'Roadway Junction Type',
     'Trafficway Description',
     'School Bus Related',
     'Work Zone',
     'Speed Limit',
     'Street or Intersection',
     'Intersection Name 1',
     'Intersection Direction 1',
     'Intersection Name 2',
     'Intersection Direction 2',
     'Intersection Name 3',
     'Intersection Direction 3',
     'Street Direction',
     'Nearest Intersection Distance',
     'Nearest Intersection Direction',
     'Landmark Distance',
     'Landmark Direction',
     'Landmark',
     'Mile Marker Direction',
     'Non Public Area',
     'Road Contributing',
     'Damaged Property Type',
     'Description of Damaged Property',
     'V1 Registration Type',
     'v1 State Code',
     'V1 Configuration',
     'V1 Emergency Response',
     'V1 Moped',
     'V1 Hit and Run',
     'V1 Action Prior to Crash',
     'V1 Model Year',
     'V1 Most Harmful Event',
     'V1 Model',
     'V1 Make',
     'V1 Occupant Count',
     'V1 Underride Override',
     'V1 First Event',
     'V1 Second Event',
     'V1 Third Event',
     'V1 Fourth Event',
     'V1 Most Damaged Area',
     'V1 Second Damaged Area',
     'V1 Third Damaged Area',
     'V1 Towed',
     'V1 Travel Direction',
     'V1 Interstate',
     'V1 Cargo Body Type',
     'V1 Gross Weight',
     'V1 Haz Placard',
     'V1 Haz Release',
     'V1 Trailer Reg Type',
     'V1 Trailer Reg Plate',
     'V1 Trailer Reg State',
     'V1 Trailer Reg Year',
     'V1 Trailer Len',
     'V1 Driver Contribution',
     'V1 Driver Contribution 2',
     'V1 Is Truck',
     'V1 Has Trailer',
     'V1 Is Bus',
     'V1 Is Hazmat',
     'V1 Reg Year',
     'V1 Driver Distracted',
     'V1 Bus Use',
     'V1 Tow Use',
     'V2 Registration Type',
     'V2 State Code',
     'V2 Configuration',
     'V2 Emergency Response',
     'V2 Moped',
     'V2 Hit and Run',
     'V2 Action Prior to Crash',
     'V2 Model Year',
     'V2 Most Harmful Event',
     'V2 Model',
     'V2 Make',
     'V2 Occupant Count',
     'V2 Underride Override',
     'V2 First Event',
     'V2 Second Event',
     'V2 Third Event',
     'V2 Fourth Event',
     'V2 Most Damaged Area',
     'V2 Second Damaged Area',
     'V2 Third Damaged Area',
     'V2 Towed',
     'V2 Travel Direction',
     'V2 Interstate',
     'V2 Cargo Body Type',
     'V2 Gross Weight',
     'V2 Haz Placard',
     'V2 Haz Release',
     'V2 Trailer Reg Type',
     'V2 Trailer Reg Plate',
     'V2 Trailer Reg State',
     'V2 Trailer Reg Year',
     'V2 Trailer Len',
     'V2 Driver Contribution',
     'V2 Driver Contribution 2',
     'V2 Is Truck',
     'V2 Has Trailer',
     'V2 Is Bus',
     'V2 Is Hazmat',
     'V2 Reg Year',
     'V2 Driver Distracted',
     'V2 Bus Use',
     'V2 Tow Use',
     'P1 Role',
     'P1 Injury',
     'P1 Drivers Lic State',
     'P1 Drivers Lic Class 1',
     'P1 Drivers Lic Class 2',
     'P1 Drivers Lic Restrict',
     'P1 Non Motorist Desc',
     'P1 Non Motorist Action',
     'P1 Non Motorist Location',
     'P1 Safety Equipment',
     'P1 Age',
     'P1 Sex',
     'P1 Seat Position',
     'P1 Safety System',
     'P1 Trapped',
     'P1 Veh Owner',
     'P2 Role',
     'P2 Injury',
     'P2 Drivers Lic State',
     'P2 Drivers Lic Class 1',
     'P2 Drivers Lic Class 2',
     'P2 Drivers Lic Restrict',
     'P2 Non Motorist Desc',
     'P2 Non Motorist Action',
     'P2 Non Motorist Location',
     'P2 Safety Equipment',
     'P2 Age',
     'P2 Sex',
     'P2 Seat Position',
     'P2 Safety System',
     'P2 Trapped',
     'P2 Veh Owner']




```python
with pandas.option_context('display.max_rows', None, 'display.max_columns', None):
    display(csv[(csv["P1 Non Motorist Desc"] == "CYCLIST") & (csv["P2 Role"] == "OPERATOR/DRIVER")])
```


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Date Time</th>
      <th>Day of Week</th>
      <th>Object 1</th>
      <th>Object 2</th>
      <th>Street Number</th>
      <th>Street Name</th>
      <th>Cross Street</th>
      <th>Near Street</th>
      <th>Location</th>
      <th>May involve cyclist</th>
      <th>May Involve Pedestrian</th>
      <th>Manner of Collision</th>
      <th>First Harmful Event Location</th>
      <th>First Harmful Event</th>
      <th>Ambient Light</th>
      <th>Weather Condition 1</th>
      <th>Weather Condition 2</th>
      <th>Traffic Control Device Type</th>
      <th>Traffic Control Device Functionality</th>
      <th>Road Surface Condition</th>
      <th>Roadway Junction Type</th>
      <th>Trafficway Description</th>
      <th>School Bus Related</th>
      <th>Work Zone</th>
      <th>Speed Limit</th>
      <th>Street or Intersection</th>
      <th>Intersection Name 1</th>
      <th>Intersection Direction 1</th>
      <th>Intersection Name 2</th>
      <th>Intersection Direction 2</th>
      <th>Intersection Name 3</th>
      <th>Intersection Direction 3</th>
      <th>Street Direction</th>
      <th>Nearest Intersection Distance</th>
      <th>Nearest Intersection Direction</th>
      <th>Landmark Distance</th>
      <th>Landmark Direction</th>
      <th>Landmark</th>
      <th>Mile Marker Direction</th>
      <th>Non Public Area</th>
      <th>Road Contributing</th>
      <th>Damaged Property Type</th>
      <th>Description of Damaged Property</th>
      <th>V1 Registration Type</th>
      <th>v1 State Code</th>
      <th>V1 Configuration</th>
      <th>V1 Emergency Response</th>
      <th>V1 Moped</th>
      <th>V1 Hit and Run</th>
      <th>V1 Action Prior to Crash</th>
      <th>V1 Model Year</th>
      <th>V1 Most Harmful Event</th>
      <th>V1 Model</th>
      <th>V1 Make</th>
      <th>V1 Occupant Count</th>
      <th>V1 Underride Override</th>
      <th>V1 First Event</th>
      <th>V1 Second Event</th>
      <th>V1 Third Event</th>
      <th>V1 Fourth Event</th>
      <th>V1 Most Damaged Area</th>
      <th>V1 Second Damaged Area</th>
      <th>V1 Third Damaged Area</th>
      <th>V1 Towed</th>
      <th>V1 Travel Direction</th>
      <th>V1 Interstate</th>
      <th>V1 Cargo Body Type</th>
      <th>V1 Gross Weight</th>
      <th>V1 Haz Placard</th>
      <th>V1 Haz Release</th>
      <th>V1 Trailer Reg Type</th>
      <th>V1 Trailer Reg Plate</th>
      <th>V1 Trailer Reg State</th>
      <th>V1 Trailer Reg Year</th>
      <th>V1 Trailer Len</th>
      <th>V1 Driver Contribution</th>
      <th>V1 Driver Contribution 2</th>
      <th>V1 Is Truck</th>
      <th>V1 Has Trailer</th>
      <th>V1 Is Bus</th>
      <th>V1 Is Hazmat</th>
      <th>V1 Reg Year</th>
      <th>V1 Driver Distracted</th>
      <th>V1 Bus Use</th>
      <th>V1 Tow Use</th>
      <th>V2 Registration Type</th>
      <th>V2 State Code</th>
      <th>V2 Configuration</th>
      <th>V2 Emergency Response</th>
      <th>V2 Moped</th>
      <th>V2 Hit and Run</th>
      <th>V2 Action Prior to Crash</th>
      <th>V2 Model Year</th>
      <th>V2 Most Harmful Event</th>
      <th>V2 Model</th>
      <th>V2 Make</th>
      <th>V2 Occupant Count</th>
      <th>V2 Underride Override</th>
      <th>V2 First Event</th>
      <th>V2 Second Event</th>
      <th>V2 Third Event</th>
      <th>V2 Fourth Event</th>
      <th>V2 Most Damaged Area</th>
      <th>V2 Second Damaged Area</th>
      <th>V2 Third Damaged Area</th>
      <th>V2 Towed</th>
      <th>V2 Travel Direction</th>
      <th>V2 Interstate</th>
      <th>V2 Cargo Body Type</th>
      <th>V2 Gross Weight</th>
      <th>V2 Haz Placard</th>
      <th>V2 Haz Release</th>
      <th>V2 Trailer Reg Type</th>
      <th>V2 Trailer Reg Plate</th>
      <th>V2 Trailer Reg State</th>
      <th>V2 Trailer Reg Year</th>
      <th>V2 Trailer Len</th>
      <th>V2 Driver Contribution</th>
      <th>V2 Driver Contribution 2</th>
      <th>V2 Is Truck</th>
      <th>V2 Has Trailer</th>
      <th>V2 Is Bus</th>
      <th>V2 Is Hazmat</th>
      <th>V2 Reg Year</th>
      <th>V2 Driver Distracted</th>
      <th>V2 Bus Use</th>
      <th>V2 Tow Use</th>
      <th>P1 Role</th>
      <th>P1 Injury</th>
      <th>P1 Drivers Lic State</th>
      <th>P1 Drivers Lic Class 1</th>
      <th>P1 Drivers Lic Class 2</th>
      <th>P1 Drivers Lic Restrict</th>
      <th>P1 Non Motorist Desc</th>
      <th>P1 Non Motorist Action</th>
      <th>P1 Non Motorist Location</th>
      <th>P1 Safety Equipment</th>
      <th>P1 Age</th>
      <th>P1 Sex</th>
      <th>P1 Seat Position</th>
      <th>P1 Safety System</th>
      <th>P1 Trapped</th>
      <th>P1 Veh Owner</th>
      <th>P2 Role</th>
      <th>P2 Injury</th>
      <th>P2 Drivers Lic State</th>
      <th>P2 Drivers Lic Class 1</th>
      <th>P2 Drivers Lic Class 2</th>
      <th>P2 Drivers Lic Restrict</th>
      <th>P2 Non Motorist Desc</th>
      <th>P2 Non Motorist Action</th>
      <th>P2 Non Motorist Location</th>
      <th>P2 Safety Equipment</th>
      <th>P2 Age</th>
      <th>P2 Sex</th>
      <th>P2 Seat Position</th>
      <th>P2 Safety System</th>
      <th>P2 Trapped</th>
      <th>P2 Veh Owner</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>639</th>
      <td>10/16/2018 10:41:00 AM</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>151</td>
      <td>CAMBRIDGE ST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>151 CAMBRIDGE ST\nCambridge, MA\n(42.370814, -...</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH MOTOR VEHICLE IN TRAFFIC</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>YES</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PARKED</td>
      <td>2010.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>RAV4</td>
      <td>TOYOTA</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LEFT SIDE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NO</td>
      <td>PAN</td>
      <td>MA</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SLOWING OR STOPPED IN TRAFFIC</td>
      <td>2008</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>I290</td>
      <td>ISUZU</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIGHT REAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>APPROACHING OR LEAVING VEHICLE</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>OTHER</td>
      <td>NONE USED - VEHICLE OCCUPANT</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>795</th>
      <td>09/12/2018 09:31:00 AM</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BRATTLE ST</td>
      <td>FARWELL PL</td>
      <td>NaN</td>
      <td>BRATTLE ST\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>RAIN</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>WET</td>
      <td>T-INTERSECTION</td>
      <td>ONE-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>BRATTLE ST</td>
      <td>NORTHBOUND</td>
      <td>FARWELL PL</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OBSTRUCTION IN ROADWAY</td>
      <td>OTHER</td>
      <td>KHS BICYCLE</td>
      <td>CON</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING RIGHT</td>
      <td>2006.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>PU</td>
      <td>FORD</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>VISIBILITY OBSTRUCTED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>SHARED-USE PATH OR TRAILS</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>797</th>
      <td>09/11/2018 03:57:00 PM</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PLEASANT ST</td>
      <td>FRANKLIN ST</td>
      <td>NaN</td>
      <td>PLEASANT ST\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>STOP SIGNS</td>
      <td>YES</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>ONE-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>PLEASANT ST</td>
      <td>SOUTHBOUND</td>
      <td>FRANKLIN ST</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>DLN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>UNKNOWN</td>
      <td>CADILLAC</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>OTHER</td>
      <td>OTHER</td>
      <td>OTHER</td>
      <td>NONE</td>
      <td>NONE</td>
      <td>NONE</td>
      <td>N</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>CYCLIST</td>
      <td>OTHER</td>
      <td>NOT IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>D, CLASS D VEHICLES</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>911</th>
      <td>08/15/2018 07:24:00 PM</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>23</td>
      <td>SIDNEY STREET</td>
      <td>NaN</td>
      <td>FRANKLIN STREET</td>
      <td>23 SIDNEY STREET\nCambridge, MA\n(42.362147, -...</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MAKING U-TURN</td>
      <td>2013.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>FUSION</td>
      <td>FORD</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LEFT SIDE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>DISREGARDED TRAFFIC SIGNS, SIGNALS, ROAD MARKINGS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>929</th>
      <td>08/08/2018 09:45:00 AM</td>
      <td>Wednesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PESCOTT STREET</td>
      <td>NaN</td>
      <td>BROADWAY STREET</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>ONE-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OVERTAKING / PASSING</td>
      <td>2017.0</td>
      <td>UNKNOWN</td>
      <td>RAV 4</td>
      <td>TOYOTA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>NaN</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1149</th>
      <td>06/13/2018 12:13:00 AM</td>
      <td>Wednesday</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNK</td>
      <td>CAMBRIDGE STREET</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SINGLE VEHICLE CRASH</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH OTHER MOVABLE OBJECT</td>
      <td>UNKNOWN</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>UNKNOWN</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>NaN</td>
      <td>COLLISION WITH OTHER MOVABLE OBJECT</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH OTHER MOVABLE OBJECT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>SHARED-USE PATH OR TRAILS</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1360</th>
      <td>04/17/2018 10:47:00 PM</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET</td>
      <td>HARDING STREET</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>REAR-END</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH MOTOR VEHICLE IN TRAFFIC</td>
      <td>DARK - LIGHTED ROADWAY</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>STOP SIGNS</td>
      <td>YES</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>CAMBRIDGE STREET</td>
      <td>NORTHBOUND</td>
      <td>HARDING STREET</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>OTHER</td>
      <td>BICYCLE</td>
      <td>PAN</td>
      <td>MA</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BACKING</td>
      <td>2005.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>EXPLORER</td>
      <td>FORD</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>REAR CENTER</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WRONG SIDE OR WRONG WAY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>VERMONT</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1386</th>
      <td>04/11/2018 10:20:00 AM</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>PORTER ROAD</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, POSITIVE MEDIAN BARRIER</td>
      <td>NO</td>
      <td>NO</td>
      <td>0</td>
      <td>INTERSECTION</td>
      <td>MASS AVE</td>
      <td>EASTBOUND</td>
      <td>PORTER ROAD</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CON</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING LEFT</td>
      <td>2016.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>300</td>
      <td>CHRYSLER</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CENTER FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1428</th>
      <td>03/29/2018 06:28:00 AM</td>
      <td>Thursday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>INMAN ST</td>
      <td>NaN</td>
      <td>BROADWAY\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DARK - LIGHTED ROADWAY</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>FOUR WAY INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>BROADWAY</td>
      <td>NORTHBOUND</td>
      <td>INMAN ST</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>OTHER</td>
      <td>DAMAGED REAR TIRE OF BIKE</td>
      <td>MVN</td>
      <td>MA</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2010.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>TRACON</td>
      <td>FORD</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LEFT SIDE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1568</th>
      <td>02/14/2018 08:16:00 PM</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OXFORD STREET</td>
      <td>EVERETT STREET</td>
      <td>NaN</td>
      <td>OXFORD STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DUSK</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>OXFORD STREET</td>
      <td>SOUTHBOUND</td>
      <td>EVERETT STREET</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OVERTAKING / PASSING</td>
      <td>2004.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>ACCENT</td>
      <td>HYUNDAI</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1938</th>
      <td>11/16/2017 02:01:00 PM</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>HARVARD ST</td>
      <td>DANA ST</td>
      <td>NaN</td>
      <td>HARVARD ST\nCambridge, MA</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>RAIN</td>
      <td>NaN</td>
      <td>STOP SIGNS</td>
      <td>YES</td>
      <td>WET</td>
      <td>FOUR WAY INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>HARVARD ST</td>
      <td>NORTHBOUND</td>
      <td>DANA ST</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING LEFT</td>
      <td>2017.0</td>
      <td>COLLISION WITH PEDESTRIAN</td>
      <td>FUSION</td>
      <td>FORD</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CENTER FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>SHARED-USE PATH OR TRAILS</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1991</th>
      <td>11/01/2017 11:15:00 AM</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET</td>
      <td>QUINCY STREET</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>UNKNOWN</td>
      <td>DARK - LIGHTED ROADWAY</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>NO</td>
      <td>DRY</td>
      <td>FOUR WAY INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>CAMBRIDGE STREET</td>
      <td>WESTBOUND</td>
      <td>QUINCY STREET</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>ENTERING TRAFFIC LANE</td>
      <td>2017.0</td>
      <td>COLLISION WITH OTHER MOVABLE OBJECT</td>
      <td>RAV 4</td>
      <td>TOYOTA</td>
      <td>3.0</td>
      <td>NaN</td>
      <td>COLLISION WITH OTHER MOVABLE OBJECT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LEFT FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>DISREGARDED TRAFFIC SIGNS, SIGNALS, ROAD MARKINGS</td>
      <td>FAILED TO YIELD THE RIGHT OF WAY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>2176</th>
      <td>09/21/2017 02:26:00 PM</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>JFK STREET</td>
      <td>MEMORIAL DRIVE</td>
      <td>NaN</td>
      <td>JFK STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH OTHER MOVABLE OBJECT</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>YES</td>
      <td>UNKNOWN</td>
      <td>FOUR WAY INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>JFK STREET</td>
      <td>EASTBOUND</td>
      <td>MEMORIAL DRIVE</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>NH</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING RIGHT</td>
      <td>2017.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>ALTIMA</td>
      <td>NISS</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>OTHER</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2203</th>
      <td>09/17/2017 02:55:00 AM</td>
      <td>Sunday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>COLUMBIA STREET</td>
      <td>BISHOP ALLEN DRIVE</td>
      <td>NaN</td>
      <td>COLUMBIA STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, OPPOSITE DIRECTION</td>
      <td>SHOULDER - PAVED</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DARK - LIGHTED ROADWAY</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>FOUR WAY INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, UNPROTECTED MEDIAN</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>COLUMBIA STREET</td>
      <td>NaN</td>
      <td>BISHOP ALLEN DRIVE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2016.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>JETTA</td>
      <td>VOLKSWAGEN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIGHT FRONT</td>
      <td>RIGHT SIDE</td>
      <td>NaN</td>
      <td>Y</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATING VEHICLE IN ERRATIC, RECKLESS, CARELESS,</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>YES OTHER REASON NOT DISABLED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>REFLECTIVE CLOTHING</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>2333</th>
      <td>08/17/2017 09:44:00 AM</td>
      <td>Thursday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>OTHER</td>
      <td>NaN</td>
      <td>MOUNT AUBURN STREET</td>
      <td>ABERDEEN AVENUE</td>
      <td>NaN</td>
      <td>MOUNT AUBURN STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, UNPROTECTED MEDIAN</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>MOUNT AUBURN STREET</td>
      <td>EASTBOUND</td>
      <td>ABERDEEN AVENUE</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNK</td>
      <td>OT</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING LEFT</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>UNK</td>
      <td>UNK</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIGHT FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNK</td>
      <td>OT</td>
      <td>OTHER</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING LEFT</td>
      <td>UNK</td>
      <td>COLLISION WITH MOTOR VEHICLE IN TRAFFIC</td>
      <td>UNK</td>
      <td>UNK</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH MOTOR VEHICLE IN TRAFFIC</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OTHER</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>DISREGARDED TRAFFIC SIGNS, SIGNALS, ROAD MARKINGS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2682</th>
      <td>05/24/2017 09:17:00 AM</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>1790</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1790 MASS AVE\nCambridge, MA\n(42.385954, -71....</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>UNKNOWN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLOUDY</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, UNPROTECTED MEDIAN</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2014.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>JETTA</td>
      <td>VOLSWAGON</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NONE</td>
      <td>NONE</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OTHER IMPROPER ACTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>2700</th>
      <td>05/21/2017 04:43:00 PM</td>
      <td>Sunday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>PLEASANT ST</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>OTHER</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>MASS AVE</td>
      <td>EASTBOUND</td>
      <td>PLEASANT ST</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2015.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>IMP</td>
      <td>SUBARU</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIGHT FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>NONE</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>NaN</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>2755</th>
      <td>05/11/2017 07:12:00 PM</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>MILTON ST</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PARKED MOTOR VEHICLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, POSITIVE MEDIAN BARRIER</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>INTERSECTION</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>MILTON ST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PARKED</td>
      <td>2007.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>JETTA</td>
      <td>VOLKSWAGEN</td>
      <td>2.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OTHER IMPROPER ACTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>NaN</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>CORRECTIVE LENSES</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>NONE USED - VEHICLE OCCUPANT</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2782</th>
      <td>05/05/2017 06:54:00 PM</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>THIRD STREET</td>
      <td>NaN</td>
      <td>THORNDIKE</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLOUDY</td>
      <td>RAIN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>WET</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2004.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>MALIBU</td>
      <td>CHEV</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LEFT FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>UNKNOWN</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>2889</th>
      <td>04/11/2017 08:46:00 AM</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>210</td>
      <td>BROADWAY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>210 BROADWAY\nCambridge, MA\n(42.366032, -71.0...</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>UNK</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CON</td>
      <td>MA</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2016.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>VAN</td>
      <td>TRANSI</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NONE</td>
      <td>NONE</td>
      <td>NONE</td>
      <td>N</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATING VEHICLE IN ERRATIC, RECKLESS, CARELESS,</td>
      <td>OPERATING VEHICLE IN ERRATIC, RECKLESS, CARELESS,</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>28.0</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2900</th>
      <td>04/08/2017 02:21:00 PM</td>
      <td>Saturday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NaN</td>
      <td>HANCOCK ST</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>REAR-END</td>
      <td>MEDIAN</td>
      <td>COLLISION WITH MOTOR VEHICLE IN TRAFFIC</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, UNPROTECTED MEDIAN</td>
      <td>NO</td>
      <td>NO</td>
      <td>25</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
      <td>MAKING U-TURN</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LEFT REAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATING VEHICLE IN ERRATIC, RECKLESS, CARELESS,</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3949</th>
      <td>08/09/2016 07:00:00 PM</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE.</td>
      <td>LINNAEAN ST.</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, POSITIVE MEDIAN BARRIER</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>MASSACHUSETTS AVE.</td>
      <td>NaN</td>
      <td>LINNAEAN ST.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING RIGHT</td>
      <td>2012.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>ACCORD</td>
      <td>HONDA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIGHT SIDE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>UNKNOWN</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>3951</th>
      <td>08/09/2016 06:16:00 PM</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>HAMPSHIRE ST</td>
      <td>NaN</td>
      <td>AMORY ST.</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>30</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>S&amp;S PARKING LOT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2013.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>FORTE</td>
      <td>KIA</td>
      <td>2.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIGHT FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>DISTRACTED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3966</th>
      <td>08/05/2016 06:39:00 PM</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>505</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>505 MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>30</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2014.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>CAMRY</td>
      <td>TOYOTA</td>
      <td>2.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>INATTENTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NaN</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>LAP BELT USED ONLY</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>4090</th>
      <td>07/06/2016 09:00:00 PM</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CONCORD AVE.</td>
      <td>FAWCETT ST.</td>
      <td>NaN</td>
      <td>CONCORD AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DUSK</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, UNPROTECTED MEDIAN</td>
      <td>NO</td>
      <td>NO</td>
      <td>30</td>
      <td>INTERSECTION</td>
      <td>CONCORD AVE.</td>
      <td>NaN</td>
      <td>FAWCETT ST.</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
      <td>TURNING RIGHT</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OTHER IMPROPER ACTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>MARKED CROSSWALK AT INTERSECTION</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4113</th>
      <td>06/29/2016 08:06:00 PM</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>LEE STREET</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, UNPROTECTED MEDIAN</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>MASS AVE</td>
      <td>WESTBOUND</td>
      <td>LEE STREET</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAS</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING LEFT</td>
      <td>2002.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>SENTRA</td>
      <td>NISSAN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CENTER FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>VISIBILITY OBSTRUCTED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NaN</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>4355</th>
      <td>05/13/2016 08:40:00 AM</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>THIRD</td>
      <td>NaN</td>
      <td>BROADWAY\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLOUDY</td>
      <td>NaN</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, POSITIVE MEDIAN BARRIER</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>BROADWAY</td>
      <td>EASTBOUND</td>
      <td>THIRD</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>OTHER</td>
      <td>BICYCLE</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2011.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>IS250</td>
      <td>LEXUS</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>COLLISION WITH MOTOR VEHICLE IN TRAFFIC</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FAILURE TO KEEP IN PROPER LANE OR RUNNING OFF ...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>CYCLIST</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NaN</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>4902</th>
      <td>12/24/2015 11:07:00 AM</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>2166</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NaN</td>
      <td>RINGE AVE</td>
      <td>2166 MASSACHUSETTS AVE\nCambridge, MA\n(42.392...</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>SLEET, HAIL, FREEZING RAIN OR DRIZZLE</td>
      <td>CLOUDY</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>WET</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, POSITIVE MEDIAN BARRIER</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>EASTBOUND</td>
      <td>40FEET</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>EASTBOUND</td>
      <td>BANK OF AMERICA ATM</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PARKED</td>
      <td>2010.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>VIBE</td>
      <td>PONTIAC</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LEFT SIDE</td>
      <td>LEFT FRONT</td>
      <td>NaN</td>
      <td>N</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>VISIBILITY OBSTRUCTED</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>CYCLIST</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>5028</th>
      <td>11/23/2015 07:57:00 AM</td>
      <td>Monday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TROWBRIDGE ST</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>ONE-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>35</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SLOWING OR STOPPED IN TRAFFIC</td>
      <td>2007.0</td>
      <td>NaN</td>
      <td>PRIUS</td>
      <td>TOYOTA</td>
      <td>2.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OTHER IMPROPER ACTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>PEDESTRIAN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NaN</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>5179</th>
      <td>10/19/2015 11:26:00 AM</td>
      <td>Monday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>BRATTLE STREET</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>Y-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, UNPROTECTED MEDIAN</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>MASS AVE</td>
      <td>WESTBOUND</td>
      <td>BRATTLE STREET</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SLOWING OR STOPPED IN TRAFFIC</td>
      <td>2007.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>`SEDAN</td>
      <td>AUDI</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>CYCLIST</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>5370</th>
      <td>09/07/2015 08:07:00 PM</td>
      <td>Monday</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CAMBRIDGE</td>
      <td>WEBSTER AVENUE</td>
      <td>NaN</td>
      <td>CAMBRIDGE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SINGLE VEHICLE CRASH</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH OTHER MOVABLE OBJECT</td>
      <td>DARK - LIGHTED ROADWAY</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>FOUR WAY INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>CAMBRIDGE</td>
      <td>EASTBOUND</td>
      <td>WEBSTER AVENUE</td>
      <td>SOUTHBOUND</td>
      <td>COLUMBIA</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNK</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>UNKNOWN</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>5398</th>
      <td>08/31/2015 04:34:00 PM</td>
      <td>Monday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MT AUBURN ST</td>
      <td>ABERDEEN AV</td>
      <td>NaN</td>
      <td>MT AUBURN ST\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>T-INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, UNPROTECTED MEDIAN</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>MT AUBURN ST</td>
      <td>WESTBOUND</td>
      <td>ABERDEEN AV</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PC</td>
      <td>ME</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING RIGHT</td>
      <td>2003.0</td>
      <td>OTHER</td>
      <td>OUTBACK</td>
      <td>SUBARU</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIGHT FRONT</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>CYCLIST</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MAINE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>5500</th>
      <td>08/04/2015 11:20:00 AM</td>
      <td>Tuesday</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>BLAKE ST</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>T-INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>BLAKE ST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>LVN</td>
      <td>MA</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING RIGHT</td>
      <td>2014.0</td>
      <td>NaN</td>
      <td>FUSION</td>
      <td>FORD</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NaN</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5557</th>
      <td>07/21/2015 12:22:00 PM</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BLAKES STREET</td>
      <td>NaN</td>
      <td>MASS. AVE</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>NaN</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>ONE-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>SOUTHBOUND</td>
      <td>10FT</td>
      <td>EASTBOUND</td>
      <td>CAMBRIDGE FIRE STATION HOUSE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CON</td>
      <td>MA</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PARKED</td>
      <td>2004.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>PU</td>
      <td>FORD</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>INATTENTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>CYCLIST</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>NONE USED - VEHICLE OCCUPANT</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>5575</th>
      <td>07/17/2015 09:06:00 AM</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>HARVARD STREET</td>
      <td>COLUMBIA STREET</td>
      <td>NaN</td>
      <td>HARVARD STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>TRAFFIC CONTROL SIGNAL</td>
      <td>YES</td>
      <td>DRY</td>
      <td>FOUR WAY INTERSECTION</td>
      <td>ONE-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>HARVARD STREET</td>
      <td>SOUTHBOUND</td>
      <td>COLUMBIA STREET</td>
      <td>EASTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAFFIC CONTROL DEVICE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2012.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>TL</td>
      <td>ACURA</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIGHT FRONT</td>
      <td>CENTER FRONT</td>
      <td>NaN</td>
      <td>N</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NO IMPROPER DRIVING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NOT DISTRACTED</td>
      <td>NaN</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NO INJURY</td>
      <td>RHODE ISLAND</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>CYCLIST</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>5935</th>
      <td>04/25/2015 04:40:00 PM</td>
      <td>Saturday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE.</td>
      <td>NaN</td>
      <td>RINDGE AVE.</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>SIDESWIPE, SAME DIRECTION</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, POSITIVE MEDIAN BARRIER</td>
      <td>NO</td>
      <td>NO</td>
      <td>30</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>OTHER</td>
      <td>BICYCLE</td>
      <td>NaN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NORTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NaN</td>
      <td>MASSACHUSETTS</td>
      <td>D, CLASS D VEHICLES</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>CYCLIST</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5964</th>
      <td>04/16/2015 10:00:00 AM</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>GARDEN ST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SHERIDAN COMMANDER</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PARKED</td>
      <td>2008.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>CROVIC</td>
      <td>FORD</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NONE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>INATTENTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>CYCLIST</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6070</th>
      <td>03/19/2015 10:54:00 AM</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NaN</td>
      <td>AMES ST</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>ANGLE</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DAYLIGHT</td>
      <td>CLEAR</td>
      <td>NaN</td>
      <td>NO CONTROLS</td>
      <td>NaN</td>
      <td>DRY</td>
      <td>NOT AT INTERSECTION</td>
      <td>TWO-WAY, DIVIDED, POSITIVE MEDIAN BARRIER</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>NON INTERSECTION</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PASS</td>
      <td>NH</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>TURNING LEFT</td>
      <td>2014.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>VOLK</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>PEDESTRIAN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>NO INJURY</td>
      <td>NEW HAMPSHIRE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6353</th>
      <td>02/07/2015 01:00:00 AM</td>
      <td>Saturday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>GREEN STREET</td>
      <td>PLEASANT STREET</td>
      <td>NaN</td>
      <td>GREEN STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>SINGLE VEHICLE CRASH</td>
      <td>ROADWAY</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>DARK - LIGHTED ROADWAY</td>
      <td>CLEAR</td>
      <td>CLEAR</td>
      <td>STOP SIGNS</td>
      <td>YES</td>
      <td>SNOW</td>
      <td>FOUR WAY INTERSECTION</td>
      <td>ONE-WAY, NOT DIVIDED</td>
      <td>NO</td>
      <td>NO</td>
      <td>NaN</td>
      <td>INTERSECTION</td>
      <td>GREEN STREET</td>
      <td>WESTBOUND</td>
      <td>PLEASANT STREET</td>
      <td>SOUTHBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OBSTRUCTION IN ROADWAY</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PAN</td>
      <td>MA</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
      <td>TRAVELING STRAIGHT AHEAD</td>
      <td>2006.0</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>ECLIPSE</td>
      <td>MITSUBISHI</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>COLLISION WITH PEDALCYCLE</td>
      <td>SEPARATION OF UNITS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>N</td>
      <td>WESTBOUND</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NON-MOTORIST</td>
      <td>NaN</td>
      <td>MASSACHUSETTS</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CYCLIST</td>
      <td>OTHER</td>
      <td>PEDESTRIAN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OPERATOR/DRIVER</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>UNKNOWN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



```python
csv["Date Time"] = csv["Date Time"].apply(pandas.to_datetime)
```


```python
csv["Date Time"]
```




    0      2019-03-30 17:08:00
    1      2019-03-29 20:49:00
    2      2019-03-29 20:21:00
    3      2019-03-29 19:22:00
    4      2019-03-29 19:07:00
    5      2019-03-29 13:35:00
    6      2019-03-29 01:36:00
    7      2019-03-28 23:10:00
    8      2019-03-28 17:23:00
    9      2019-03-28 16:11:00
    10     2019-03-28 08:54:00
    11     2019-03-28 00:17:00
    12     2019-03-27 18:00:00
    13     2019-03-27 16:51:00
    14     2019-03-27 12:15:00
    15     2019-03-27 07:39:00
    16     2019-03-26 22:46:00
    17     2019-03-26 14:44:00
    18     2019-03-26 12:15:00
    19     2019-03-25 21:39:00
    20     2019-03-25 10:37:00
    21     2019-03-25 09:05:00
    22     2019-03-25 06:19:00
    23     2019-03-24 13:00:00
    24     2019-03-23 17:14:00
    25     2019-03-22 11:09:00
    26     2019-03-22 10:11:00
    27     2019-03-22 09:18:00
    28     2019-03-21 19:43:00
    29     2019-03-21 18:08:00
                   ...        
    6496   2015-01-09 19:03:00
    6497   2015-01-09 17:22:00
    6498   2015-01-09 07:24:00
    6499   2015-01-08 21:43:00
    6500   2015-01-08 14:19:00
    6501   2015-01-08 08:47:00
    6502   2015-01-07 21:25:00
    6503   2015-01-07 15:25:00
    6504   2015-01-07 13:45:00
    6505   2015-01-07 10:28:00
    6506   2015-01-07 00:42:00
    6507   2015-01-06 23:30:00
    6508   2015-01-06 18:18:00
    6509   2015-01-06 10:45:00
    6510   2015-01-05 21:53:00
    6511   2015-01-05 18:24:00
    6512   2015-01-05 12:50:00
    6513   2015-01-05 10:00:00
    6514   2015-01-05 09:17:00
    6515   2015-01-05 09:15:00
    6516   2015-01-04 06:24:00
    6517   2015-01-03 19:48:00
    6518   2015-01-02 12:35:00
    6519   2015-01-01 22:52:00
    6520   2015-01-01 11:00:00
    6521   2015-01-01 06:52:00
    6522   2015-01-01 04:14:00
    6523   2015-01-01 01:54:00
    6524   2015-01-01 01:12:00
    6525   2015-01-01 00:45:00
    Name: Date Time, Length: 6526, dtype: datetime64[ns]




```python

```


```python
from datetime import datetime
councilterm = csv[csv["Date Time"] >= datetime(2018, 1, 1)]
councilterm["Date Time"]
```




    0      2019-03-30 17:08:00
    1      2019-03-29 20:49:00
    2      2019-03-29 20:21:00
    3      2019-03-29 19:22:00
    4      2019-03-29 19:07:00
    5      2019-03-29 13:35:00
    6      2019-03-29 01:36:00
    7      2019-03-28 23:10:00
    8      2019-03-28 17:23:00
    9      2019-03-28 16:11:00
    10     2019-03-28 08:54:00
    11     2019-03-28 00:17:00
    12     2019-03-27 18:00:00
    13     2019-03-27 16:51:00
    14     2019-03-27 12:15:00
    15     2019-03-27 07:39:00
    16     2019-03-26 22:46:00
    17     2019-03-26 14:44:00
    18     2019-03-26 12:15:00
    19     2019-03-25 21:39:00
    20     2019-03-25 10:37:00
    21     2019-03-25 09:05:00
    22     2019-03-25 06:19:00
    23     2019-03-24 13:00:00
    24     2019-03-23 17:14:00
    25     2019-03-22 11:09:00
    26     2019-03-22 10:11:00
    27     2019-03-22 09:18:00
    28     2019-03-21 19:43:00
    29     2019-03-21 18:08:00
                   ...        
    1732   2018-01-05 21:48:00
    1733   2018-01-05 17:38:00
    1734   2018-01-05 16:16:00
    1735   2018-01-05 15:18:00
    1736   2018-01-05 14:38:00
    1737   2018-01-05 13:37:00
    1738   2018-01-05 12:42:00
    1739   2018-01-05 11:18:00
    1740   2018-01-05 11:03:00
    1741   2018-01-05 08:47:00
    1742   2018-01-04 20:00:00
    1743   2018-01-04 16:02:00
    1744   2018-01-04 15:30:00
    1745   2018-01-04 12:51:00
    1746   2018-01-03 22:07:00
    1747   2018-01-03 20:55:00
    1748   2018-01-03 17:03:00
    1749   2018-01-03 09:27:00
    1750   2018-01-03 08:19:00
    1751   2018-01-02 20:29:00
    1752   2018-01-02 18:50:00
    1753   2018-01-02 18:18:00
    1754   2018-01-02 13:10:00
    1755   2018-01-02 12:22:00
    1756   2018-01-02 10:43:00
    1757   2018-01-01 22:36:00
    1758   2018-01-01 21:42:00
    1759   2018-01-01 18:43:00
    1760   2018-01-01 11:16:00
    1761   2018-01-01 05:11:00
    Name: Date Time, Length: 1762, dtype: datetime64[ns]




```python
sum(councilterm["V2 Model"] == "BIKE")
```




    1




```python
councilterm = councilterm.fillna({"P2 Non Motorist Desc": "", "P1 Non Motorist Desc": "", "May involve cyclist": 0, "Object 1": "", "P1 Injury": "", "P2 Injury": ""})
cyclists = councilterm[(councilterm["May involve cyclist"] > 0) & (councilterm["Object 1"] != "") & (
    (councilterm["P2 Non Motorist Desc"] == "CYCLIST") | (councilterm["P1 Non Motorist Desc"] == "CYCLIST"))]
cyclists
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Date Time</th>
      <th>Day of Week</th>
      <th>Object 1</th>
      <th>Object 2</th>
      <th>Street Number</th>
      <th>Street Name</th>
      <th>Cross Street</th>
      <th>Near Street</th>
      <th>Location</th>
      <th>May involve cyclist</th>
      <th>...</th>
      <th>P2 Non Motorist Desc</th>
      <th>P2 Non Motorist Action</th>
      <th>P2 Non Motorist Location</th>
      <th>P2 Safety Equipment</th>
      <th>P2 Age</th>
      <th>P2 Sex</th>
      <th>P2 Seat Position</th>
      <th>P2 Safety System</th>
      <th>P2 Trapped</th>
      <th>P2 Veh Owner</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>8</th>
      <td>2019-03-28 17:23:00</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>2343</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>SHEA ROAD</td>
      <td>2343 MASS AVE\nCambridge, MA\n(42.396067, -71....</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>35</th>
      <td>2019-03-19 08:47:00</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>PROSPECT STREET</td>
      <td>NaN</td>
      <td>BROADWAY\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>46</th>
      <td>2019-03-15 20:00:00</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OXFORD STREET</td>
      <td>NaN</td>
      <td>SACRAMENTO STREET</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>REFLECTIVE CLOTHING</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>52</th>
      <td>2019-03-13 13:18:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>ALBANY ST</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>118</th>
      <td>2019-02-24 19:08:00</td>
      <td>Sunday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>1525</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NaN</td>
      <td>WATERHOUSE AVE</td>
      <td>1525 MASSACHUSETTS AVE\nCambridge, MA\n(42.377...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>145</th>
      <td>2019-02-15 19:07:00</td>
      <td>Friday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>201</td>
      <td>BROADWAY</td>
      <td>NaN</td>
      <td>PORTLAND STREET</td>
      <td>201 BROADWAY\nCambridge, MA\n(42.36599, -71.09...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>150</th>
      <td>2019-02-14 17:44:00</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>BLAKE STREET</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>SHARED-USE PATH OR TRAILS</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>165</th>
      <td>2019-02-11 11:20:00</td>
      <td>Monday</td>
      <td>UNKNOWN HEAVY TRUCK</td>
      <td>NaN</td>
      <td>259</td>
      <td>CAMBRIDGE ST</td>
      <td>NaN</td>
      <td>THIRD ST</td>
      <td>259 CAMBRIDGE ST\nCambridge, MA\n(42.371076, -...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>191</th>
      <td>2019-02-05 18:48:00</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PORTLAND STREET</td>
      <td>NaN</td>
      <td>ALBANY STREET</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>REFLECTIVE CLOTHING</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>223</th>
      <td>2019-01-28 12:22:00</td>
      <td>Monday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>ELLERY ST</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>268</th>
      <td>2019-01-16 14:59:00</td>
      <td>Wednesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>DUDLEY ST</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>361</th>
      <td>2018-12-16 11:14:00</td>
      <td>Sunday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>DAY ST</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>SHARED-USE PATH OR TRAILS</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>397</th>
      <td>2018-12-10 14:50:00</td>
      <td>Monday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BEACON</td>
      <td>ANTRIM</td>
      <td>NaN</td>
      <td>BEACON\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>399</th>
      <td>2018-12-09 19:42:00</td>
      <td>Sunday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RITE AID PARKING LOT</td>
      <td>RIVER STREET</td>
      <td>NaN</td>
      <td>RITE AID PARKING LOT\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>SIDEWALK</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>412</th>
      <td>2018-12-07 13:35:00</td>
      <td>Friday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>TREMONT</td>
      <td>NaN</td>
      <td>BROADWAY\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>434</th>
      <td>2018-12-04 09:21:00</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>HAMPSHIRE STREET</td>
      <td>PROSPECT STREET</td>
      <td>NaN</td>
      <td>HAMPSHIRE STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>437</th>
      <td>2018-12-03 08:44:00</td>
      <td>Monday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CAMERON AV</td>
      <td>FAIR OAKS</td>
      <td>NaN</td>
      <td>CAMERON AV\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>449</th>
      <td>2018-11-29 22:36:00</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>FRONT STREET</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>453</th>
      <td>2018-11-28 19:49:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MAGAZINE STREET</td>
      <td>NaN</td>
      <td>PUTNAM AVE</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>455</th>
      <td>2018-11-28 12:12:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>FELTON</td>
      <td>NaN</td>
      <td>BROADWAY\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>REFLECTIVE CLOTHING</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>460</th>
      <td>2018-11-27 12:33:00</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CAMBRIDGE ST</td>
      <td>ELLERY ST</td>
      <td>NaN</td>
      <td>CAMBRIDGE ST\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>463</th>
      <td>2018-11-25 16:40:00</td>
      <td>Sunday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSCHUSETTS AVENUE</td>
      <td>AMHERST STREET</td>
      <td>NaN</td>
      <td>MASSCHUSETTS AVENUE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>AT INTERSECTION BUT NO CROSSWALK</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>523</th>
      <td>2018-11-13 11:36:00</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>1564</td>
      <td>CAMBRIDGE STREET</td>
      <td>NaN</td>
      <td>DANA STREET</td>
      <td>1564 CAMBRIDGE STREET\nCambridge, MA\n(42.3745...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>543</th>
      <td>2018-11-08 09:50:00</td>
      <td>Thursday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>2200</td>
      <td>MASSACHUSETTS AVE./RICE STREET</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2200 MASSACHUSETTS AVE RICE STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>545</th>
      <td>2018-11-07 18:37:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>OTHER</td>
      <td>NaN</td>
      <td>BAY</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NaN</td>
      <td>BAY\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>27.0</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>546</th>
      <td>2018-11-07 15:08:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>THIRD STREET</td>
      <td>HURLEY STREET</td>
      <td>NaN</td>
      <td>THIRD STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>OTHER</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>581</th>
      <td>2018-10-30 10:42:00</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>600</td>
      <td>MAIN ST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>600 MAIN ST\nCambridge, MA\n(42.362833, -71.09...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>597</th>
      <td>2018-10-25 18:19:00</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>LEE STREET</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>SHOULDER</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>620</th>
      <td>2018-10-20 08:22:00</td>
      <td>Saturday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>HAMPSHIRE STREET</td>
      <td>BROADWAY</td>
      <td>NaN</td>
      <td>HAMPSHIRE STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>629</th>
      <td>2018-10-18 18:38:00</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NaN</td>
      <td>RUSSELL STREET</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>SHOULDER</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1156</th>
      <td>2018-06-11 08:42:00</td>
      <td>Monday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>60</td>
      <td>BINNEY ST</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>60 BINNEY ST\nCambridge, MA\n(42.365076, -71.0...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1162</th>
      <td>2018-06-08 17:31:00</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>SOMERVILLE AVE</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1176</th>
      <td>2018-06-05 11:16:00</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CONCORD AVE</td>
      <td>NaN</td>
      <td>FAWCETT STREET</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1233</th>
      <td>2018-05-23 13:39:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BRATTLE STREET</td>
      <td>NaN</td>
      <td>HAWTHORNE STREET</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1283</th>
      <td>2018-05-07 20:31:00</td>
      <td>Monday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MAIN STREET</td>
      <td>VASSAR STREET</td>
      <td>NaN</td>
      <td>MAIN STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>MARKED CROSSWALK AT INTERSECTION</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1286</th>
      <td>2018-05-07 12:24:00</td>
      <td>Monday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CONCORD AV</td>
      <td>CHAUNCY ST</td>
      <td>NaN</td>
      <td>CONCORD AV\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>AT INTERSECTION BUT NO CROSSWALK</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1289</th>
      <td>2018-05-04 20:53:00</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>SIDNEY STREET</td>
      <td>MASSACHUSETTS AVENUE</td>
      <td>NaN</td>
      <td>SIDNEY STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1290</th>
      <td>2018-05-04 17:49:00</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AV</td>
      <td>NEWPORT RD</td>
      <td>NaN</td>
      <td>MASS AV\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1291</th>
      <td>2018-05-04 17:37:00</td>
      <td>Friday</td>
      <td>SINGLE UNIT TRUCK (2 AXLES, 6 TIRES)</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MT.AUBURN STREET</td>
      <td>NaN</td>
      <td>DEWOLFE STREET</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1303</th>
      <td>2018-05-02 17:30:00</td>
      <td>Wednesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>RIVER ST</td>
      <td>KINNAIRD ST</td>
      <td>NaN</td>
      <td>RIVER ST\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1306</th>
      <td>2018-05-01 22:38:00</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PEABODY ST.</td>
      <td>MASS.  AVE.</td>
      <td>NaN</td>
      <td>PEABODY ST\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1326</th>
      <td>2018-04-26 09:48:00</td>
      <td>Thursday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>VASSAR STREET</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>VASSAR STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1351</th>
      <td>2018-04-19 22:23:00</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>32</td>
      <td>VASSAR STREET</td>
      <td>NaN</td>
      <td>MAIN STREET</td>
      <td>32 VASSAR STREET\nCambridge, MA\n(42.361318, -...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1358</th>
      <td>2018-04-18 14:04:00</td>
      <td>Wednesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CAMBRIDGE ST</td>
      <td>SIXTH ST</td>
      <td>NaN</td>
      <td>CAMBRIDGE ST\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1360</th>
      <td>2018-04-17 22:47:00</td>
      <td>Tuesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET</td>
      <td>HARDING STREET</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1374</th>
      <td>2018-04-14 18:21:00</td>
      <td>Saturday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>176</td>
      <td>SHERMAN ST</td>
      <td>NaN</td>
      <td>RINDGE AVE</td>
      <td>176 SHERMAN ST\nCambridge, MA\n(42.39212, -71....</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1386</th>
      <td>2018-04-11 10:20:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>PORTER ROAD</td>
      <td>NaN</td>
      <td>MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>FRONT SEAT - LEFT SIDE, OR MOTORCYLE DRIVER</td>
      <td>SHOULDER AND LAP BELT USED</td>
      <td>NOT TRAPPED</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1402</th>
      <td>2018-04-06 10:07:00</td>
      <td>Friday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>1712</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>MARTIN STREET</td>
      <td>1712 MASS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1404</th>
      <td>2018-04-05 16:30:00</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>2094</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NaN</td>
      <td>WALDEN ST</td>
      <td>2094 MASSACHUSETTS AVE\nCambridge, MA\n(42.391...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1406</th>
      <td>2018-04-04 19:26:00</td>
      <td>Wednesday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>2</td>
      <td>EDUCATION CIRCLE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2 EDUCATION CIRCLE\nCambridge, MA\n(42.369401,...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1428</th>
      <td>2018-03-29 06:28:00</td>
      <td>Thursday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>INMAN ST</td>
      <td>NaN</td>
      <td>BROADWAY\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1435</th>
      <td>2018-03-27 10:49:00</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>WASHBURN AVE</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1447</th>
      <td>2018-03-24 17:36:00</td>
      <td>Saturday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>PROSPECT STREET</td>
      <td>NaN</td>
      <td>HAMPSHIRE STREET</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>NONE USED</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1481</th>
      <td>2018-03-15 09:12:00</td>
      <td>Thursday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>133</td>
      <td>PUTNAM AVE</td>
      <td>NaN</td>
      <td>MAGEE STREET</td>
      <td>133 PUTNAM AVE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1520</th>
      <td>2018-03-06 12:37:00</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>ELLERY STREET</td>
      <td>NaN</td>
      <td>BROADWAY\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1559</th>
      <td>2018-02-20 15:15:00</td>
      <td>Tuesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVENUE</td>
      <td>TROWBRIDGE STREET</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVENUE\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>SHARED-USE PATH OR TRAILS</td>
      <td>UNKNOWN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1568</th>
      <td>2018-02-14 20:16:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>OXFORD STREET</td>
      <td>EVERETT STREET</td>
      <td>NaN</td>
      <td>OXFORD STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1592</th>
      <td>2018-02-07 19:30:00</td>
      <td>Wednesday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>WATERHOUSE ST</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>...</td>
      <td></td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Y</td>
    </tr>
    <tr>
      <th>1604</th>
      <td>2018-02-05 18:15:00</td>
      <td>Monday</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>KIRKLAND STREET</td>
      <td>ROBERTS RD</td>
      <td>NaN</td>
      <td>KIRKLAND STREET\nCambridge, MA</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>ENTERING OR CROSSING SPECIFIED LOCATION</td>
      <td>NaN</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>FEMALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1696</th>
      <td>2018-01-12 08:59:00</td>
      <td>Friday</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>1400</td>
      <td>MASS AVE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1400 MASS AVE\nCambridge, MA\n(42.37344, -71.1...</td>
      <td>1.0</td>
      <td>...</td>
      <td>CYCLIST</td>
      <td>WALKING, RUNNING OR CYCLING</td>
      <td>IN ROADWAY</td>
      <td>HELMET</td>
      <td>NaN</td>
      <td>MALE</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>108 rows × 159 columns</p>
</div>




```python
summary = cyclists[["Date Time", "Object 1", "Object 2", "Street Name", "P1 Injury", "P1 Non Motorist Desc", "P2 Injury", "P2 Non Motorist Desc"]]
summary = summary[(summary["P2 Injury"] != "NO INJURY") | (summary["P1 Injury"] != "NO INJURY")]
print(len(list(summary.iterrows())))
with pandas.option_context('display.max_rows', None, 'display.max_columns', None):
    display(summary)
```

    87



<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Date Time</th>
      <th>Object 1</th>
      <th>Object 2</th>
      <th>Street Name</th>
      <th>P1 Injury</th>
      <th>P1 Non Motorist Desc</th>
      <th>P2 Injury</th>
      <th>P2 Non Motorist Desc</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>8</th>
      <td>2019-03-28 17:23:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>35</th>
      <td>2019-03-19 08:47:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>46</th>
      <td>2019-03-15 20:00:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>OXFORD STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>52</th>
      <td>2019-03-13 13:18:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>118</th>
      <td>2019-02-24 19:08:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>165</th>
      <td>2019-02-11 11:20:00</td>
      <td>UNKNOWN HEAVY TRUCK</td>
      <td>NaN</td>
      <td>CAMBRIDGE ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>191</th>
      <td>2019-02-05 18:48:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>PORTLAND STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>223</th>
      <td>2019-01-28 12:22:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>268</th>
      <td>2019-01-16 14:59:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>361</th>
      <td>2018-12-16 11:14:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>UNKNOWN</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>399</th>
      <td>2018-12-09 19:42:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>RITE AID PARKING LOT</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>412</th>
      <td>2018-12-07 13:35:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NO INJURY</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>434</th>
      <td>2018-12-04 09:21:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>HAMPSHIRE STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>437</th>
      <td>2018-12-03 08:44:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>CAMERON AV</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>449</th>
      <td>2018-11-29 22:36:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>455</th>
      <td>2018-11-28 12:12:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>463</th>
      <td>2018-11-25 16:40:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSCHUSETTS AVENUE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>543</th>
      <td>2018-11-08 09:50:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE./RICE STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>581</th>
      <td>2018-10-30 10:42:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>MAIN ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>597</th>
      <td>2018-10-25 18:19:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>639</th>
      <td>2018-10-16 10:41:00</td>
      <td>PASSENGER CAR</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>CAMBRIDGE ST</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
      <td>NO INJURY</td>
      <td></td>
    </tr>
    <tr>
      <th>671</th>
      <td>2018-10-10 11:37:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>FAWCETT ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>674</th>
      <td>2018-10-09 18:18:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>PACIFIC</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>718</th>
      <td>2018-09-28 17:02:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>MASS AVENUE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>728</th>
      <td>2018-09-26 18:00:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>DANA STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>741</th>
      <td>2018-09-24 21:30:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>QUINCY ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>UNKNOWN</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>766</th>
      <td>2018-09-19 16:10:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>CARDINAL MEDEIROS</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>779</th>
      <td>2018-09-15 19:49:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MAIN ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>795</th>
      <td>2018-09-12 09:31:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>BRATTLE ST</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
      <td>NO INJURY</td>
      <td></td>
    </tr>
    <tr>
      <th>817</th>
      <td>2018-09-07 18:51:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MAIN STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>835</th>
      <td>2018-09-04 10:00:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>836</th>
      <td>2018-09-04 09:45:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>838</th>
      <td>2018-09-03 12:20:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>GREEN ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>856</th>
      <td>2018-08-30 00:12:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>857</th>
      <td>2018-08-29 20:45:00</td>
      <td>SINGLE UNIT TRUCK (2 AXLES, 6 TIRES)</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>863</th>
      <td>2018-08-29 11:29:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>ALEWIFE STATION ACCESS ROAD</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>876</th>
      <td>2018-08-26 16:19:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>PLEASANT ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>891</th>
      <td>2018-08-22 08:43:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>HAMPSHIRE ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>901</th>
      <td>2018-08-19 16:56:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>COLUBIA STREET</td>
      <td></td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>908</th>
      <td>2018-08-16 14:55:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MT. AUBURN STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>909</th>
      <td>2018-08-16 09:15:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>ELLERY STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>911</th>
      <td>2018-08-15 19:24:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>SIDNEY STREET</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
      <td>NO INJURY</td>
      <td></td>
    </tr>
    <tr>
      <th>915</th>
      <td>2018-08-14 11:55:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>940</th>
      <td>2018-08-07 10:41:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>944</th>
      <td>2018-08-06 21:08:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>945</th>
      <td>2018-08-06 19:35:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>VASSAR STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>988</th>
      <td>2018-07-27 11:37:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>NORFOLK ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>989</th>
      <td>2018-07-26 23:09:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1003</th>
      <td>2018-07-25 09:14:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>ALBANY STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1012</th>
      <td>2018-07-20 08:44:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1014</th>
      <td>2018-07-19 18:43:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
      <td>UNKNOWN</td>
      <td></td>
    </tr>
    <tr>
      <th>1018</th>
      <td>2018-07-19 09:11:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>BRATTLE ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1050</th>
      <td>2018-07-11 19:13:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>UNKNOWN</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1087</th>
      <td>2018-06-27 10:20:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1097</th>
      <td>2018-06-26 14:08:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>UNKNOWN</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1100</th>
      <td>2018-06-26 11:58:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>FRANKLIN ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1120</th>
      <td>2018-06-20 14:00:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>CAMBRIDGE ST</td>
      <td></td>
      <td></td>
      <td>NO INJURY</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1145</th>
      <td>2018-06-13 16:18:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>HARVARD STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1148</th>
      <td>2018-06-13 09:59:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE.</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1152</th>
      <td>2018-06-11 18:21:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>WALDEN STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1156</th>
      <td>2018-06-11 08:42:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>BINNEY ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1162</th>
      <td>2018-06-08 17:31:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>NO INJURY</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>1176</th>
      <td>2018-06-05 11:16:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>CONCORD AVE</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>1283</th>
      <td>2018-05-07 20:31:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MAIN STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1286</th>
      <td>2018-05-07 12:24:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>CONCORD AV</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1289</th>
      <td>2018-05-04 20:53:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>SIDNEY STREET</td>
      <td>NON FATAL INJURY - INCAPACITATING</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>1290</th>
      <td>2018-05-04 17:49:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASS AV</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1291</th>
      <td>2018-05-04 17:37:00</td>
      <td>SINGLE UNIT TRUCK (2 AXLES, 6 TIRES)</td>
      <td>NaN</td>
      <td>MT.AUBURN STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1303</th>
      <td>2018-05-02 17:30:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>RIVER ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1306</th>
      <td>2018-05-01 22:38:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>PEABODY ST.</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>1326</th>
      <td>2018-04-26 09:48:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>VASSAR STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1351</th>
      <td>2018-04-19 22:23:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>VASSAR STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1358</th>
      <td>2018-04-18 14:04:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>CAMBRIDGE ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>UNKNOWN</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1360</th>
      <td>2018-04-17 22:47:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>CAMBRIDGE STREET</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
      <td>NO INJURY</td>
      <td></td>
    </tr>
    <tr>
      <th>1374</th>
      <td>2018-04-14 18:21:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>SHERMAN ST</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1404</th>
      <td>2018-04-05 16:30:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1406</th>
      <td>2018-04-04 19:26:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>EDUCATION CIRCLE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1428</th>
      <td>2018-03-29 06:28:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
      <td>NO INJURY</td>
      <td></td>
    </tr>
    <tr>
      <th>1435</th>
      <td>2018-03-27 10:49:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1447</th>
      <td>2018-03-24 17:36:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>PROSPECT STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1481</th>
      <td>2018-03-15 09:12:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>PUTNAM AVE</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>1520</th>
      <td>2018-03-06 12:37:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>BROADWAY</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>1559</th>
      <td>2018-02-20 15:15:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASSACHUSETTS AVENUE</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1568</th>
      <td>2018-02-14 20:16:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>OXFORD STREET</td>
      <td>NON FATAL INJURY - NON INCAPACITATING</td>
      <td>CYCLIST</td>
      <td>NO INJURY</td>
      <td></td>
    </tr>
    <tr>
      <th>1592</th>
      <td>2018-02-07 19:30:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>NO INJURY</td>
      <td>CYCLIST</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <th>1604</th>
      <td>2018-02-05 18:15:00</td>
      <td>PASSENGER CAR</td>
      <td>NaN</td>
      <td>KIRKLAND STREET</td>
      <td>NO INJURY</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
    <tr>
      <th>1696</th>
      <td>2018-01-12 08:59:00</td>
      <td>LIGHT TRUCK(VAN, MINI VAN, PICK-UP, SPORT UTIL...</td>
      <td>NaN</td>
      <td>MASS AVE</td>
      <td>UNKNOWN</td>
      <td></td>
      <td>NON FATAL INJURY - POSSIBLE</td>
      <td>CYCLIST</td>
    </tr>
  </tbody>
</table>
</div>



```python
for _, (dt, vehicle, _, street, injury1, _, injury2, _) in reversed(list(summary.iterrows())):
    date = dt.date()
    injury = injury1 if injury1 != "NO INJURY" else injury2
    if vehicle.startswith("LIGHT TRUCK"):
        vehicle = "LIGHT TRUCK"
    if injury in ("NON FATAL INJURY - POSSIBLE", "UNKNOWN", ""):
        continue
    if injury == "NON FATAL INJURY - NON INCAPACITATING":
        injury = ""
    if injury == "NON FATAL INJURY - INCAPACITATING":
        injury = ", injury was incapacitating"
    
    print(f"On {date} at {street} the driver of a {vehicle} hit and injured a bicycle rider{injury}")
```

    On 2018-02-14 at OXFORD STREET the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-02-20 at MASSACHUSETTS AVENUE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-03-06 at BROADWAY the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-03-15 at PUTNAM AVE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-04-05 at MASSACHUSETTS AVE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-04-17 at CAMBRIDGE STREET the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-04-19 at VASSAR STREET the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-04-26 at VASSAR STREET the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-05-02 at RIVER ST the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-05-04 at MT.AUBURN STREET the driver of a SINGLE UNIT TRUCK (2 AXLES, 6 TIRES) hit and injured a bicycle rider
    On 2018-05-04 at MASS AV the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-05-04 at SIDNEY STREET the driver of a PASSENGER CAR hit and injured a bicycle rider, injury was incapacitating
    On 2018-05-07 at CONCORD AV the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-06-05 at CONCORD AVE the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-06-11 at BINNEY ST the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-06-13 at MASSACHUSETTS AVE. the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-06-13 at HARVARD STREET the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-06-26 at FRANKLIN ST the driver of a PASSENGER CAR hit and injured a bicycle rider, injury was incapacitating
    On 2018-06-27 at BROADWAY the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-07-19 at BRATTLE ST the driver of a LIGHT TRUCK hit and injured a bicycle rider, injury was incapacitating
    On 2018-07-19 at BROADWAY the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-07-27 at NORFOLK ST the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-08-06 at BROADWAY the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-08-14 at MASSACHUSETTS AVE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-08-22 at HAMPSHIRE ST the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-08-26 at PLEASANT ST the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-08-29 at ALEWIFE STATION ACCESS ROAD the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-08-29 at MASSACHUSETTS AVE the driver of a SINGLE UNIT TRUCK (2 AXLES, 6 TIRES) hit and injured a bicycle rider
    On 2018-09-03 at GREEN ST the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-09-04 at MASSACHUSETTS AVE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-09-04 at CAMBRIDGE STREET the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-09-15 at MAIN ST the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-09-19 at CARDINAL MEDEIROS the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-09-26 at DANA STREET the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-09-28 at MASS AVENUE the driver of a LIGHT TRUCK hit and injured a bicycle rider, injury was incapacitating
    On 2018-10-09 at PACIFIC the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-10-16 at CAMBRIDGE ST the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-10-30 at MAIN ST the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-11-08 at MASSACHUSETTS AVE./RICE STREET the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-11-25 at MASSCHUSETTS AVENUE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-11-28 at BROADWAY the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-11-29 at MASSACHUSETTS AVE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-12-03 at CAMERON AV the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2018-12-04 at HAMPSHIRE STREET the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2018-12-09 at RITE AID PARKING LOT the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2019-01-16 at MASSACHUSETTS AVE the driver of a LIGHT TRUCK hit and injured a bicycle rider
    On 2019-01-28 at MASSACHUSETTS AVE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2019-02-11 at CAMBRIDGE ST the driver of a UNKNOWN HEAVY TRUCK hit and injured a bicycle rider
    On 2019-02-24 at MASSACHUSETTS AVE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2019-03-13 at MASSACHUSETTS AVE the driver of a PASSENGER CAR hit and injured a bicycle rider
    On 2019-03-28 at MASS AVE the driver of a PASSENGER CAR hit and injured a bicycle rider


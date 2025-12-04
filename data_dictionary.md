# Data Dictionary - Transit Regina Cleaned Dataset

## Final Tidy Dataset: `clean_stops`

| Column Name | Data Type | Description | Units/Format | Example |
|-------------|-----------|-------------|--------------|---------|
| `stop_id` | int32 | Unique identifier for bus stop | Integer | 1001 |
| `stop_name` | object | Official name of bus stop | Uppercase text | "UNIVERSITY PARK DR @ QUANCE ST" |
| `on_street` | object | Primary street location | Uppercase text | "UNIVERSITY PARK DR" |
| `at_street` | object | Cross street location | Uppercase text | "QUANCE ST (NB)" |
| `lat` | object | Latitude coordinate | Decimal degrees | "50.444" |
| `lon` | object | Longitude coordinate | Decimal degrees | "-104.549" |
| `global_id` | object | Global unique identifier | UUID | "{ABC-123-DEF}" |
| `object_id` | int64 | GIS object identifier | Integer | 59930 |
| `region` | object | Geographic quadrant of Regina | NE/NW/SE/SW | "NW" |
| `distance_from_center_km` | float64 | Distance from city center | Kilometers | 5.234 |

## GTFS Dataset: `times_gtfs_clean`

| Column Name | Data Type | Description | Units/Format | Example |
|-------------|-----------|-------------|--------------|---------|
| `trip_id` | object | Unique trip identifier | Uppercase text | "TRIP_12345" |
| `arrival_time` | object | Scheduled arrival time | HH:MM:SS | "08:30:00" |
| `departure_time` | object | Scheduled departure time | HH:MM:SS | "08:30:30" |
| `stop_id` | int64 | Stop identifier (FK) | Integer | 1001 |
| `stop_sequence` | int64 | Order of stop on route | Integer (1-n) | 5 |
| `arrival_datetime` | datetime64 | Parsed arrival timestamp | Datetime | 2024-01-01 08:30:00 |
| `departure_datetime` | datetime64 | Parsed departure timestamp | Datetime | 2024-01-01 08:30:30 |
| `arrival_hour` | int64 | Hour of arrival (derived) | 0-23 | 8 |
| `arrival_minute` | int64 | Minute of arrival (derived) | 0-59 | 30 |

## Aggregated Dataset: `region_summary`

| Column Name | Data Type | Description | Units/Format |
|-------------|-----------|-------------|--------------|
| `region` | object | Geographic quadrant | NE/NW/SE/SW |
| `num_stops` | int64 | Count of stops in region | Integer |
| `avg_distance_km` | float64 | Average distance from center | Kilometers |
| `max_distance_km` | float64 | Maximum distance from center | Kilometers |
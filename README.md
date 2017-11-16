# log_file_timetracking_script

## Requirements:
* install jq (brew install jq)
* install parallel (brew install parallel)
* install coreutils (gdate is needed) (brew install coreutils)
* install moreutils (without parallel in order to avoid conflict with previous installed parallel) (brew install moreutils --without-parallel)
* create file(or symlink) for tracking data: 
  `ln -s ~/<file> ~/.time_tracking_from_logfiles`
* add bin folder to PATH variable

## Commands
* get time tracking data from log files and write to ~/.time_tracking_from_logfiles:
  `time_tracking_from_logfiles update`
* show tracked time of this week
  `time_tracking_from_logfiles this_week`
* show average of last 3 weeks
  `time_tracking_from_logfiles last_weeks`



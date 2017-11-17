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

## Example Output

    work_time_per_week=40 working_time_file="<PATH>/log_file_timetracking_script/example_data.json" time_tracking_from_logfiles this_week
    {"date":"2017-11-13","start":"09:17:30","stop":"17:51:56","duration":8.56}
    {"date":"2017-11-14","start":"08:48:14","stop":"17:08:56","duration":8.33}
    {"date":"2017-11-15","start":"10:19:41","stop":"18:22:36","duration":8.05}
    {"date":"2017-11-16","start":"08:59:06","stop":"17:15:55","duration":8.26}
    {"date":"2017-11-17","start":"08:59:21","stop":"16:00:00","duration":7.01}
    {"total":40.21,"overtime":0.21}


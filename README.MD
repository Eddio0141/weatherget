# What is weatherget?
weatherget is a small Python script that generates two text files, if they don't exist already (current_weather.txt and current_time.txt) and continuously updates both with the time and weather of the specified place. This is useful as a livestreaming tool that can be self-hosted on your home PC.

# How to use weathertimeget.py
- Obtain free weather API key from https://home.openweathermap.org/users/sign_up
- Add desired city's weather and time. You can do this by looking up on Google "city latitude and longitude"\
For example, "Montreal latitude and longitude". Copy these values into the lat and lon parameters of settings.json
- You may add as many cities as you want, as long as you follow the format of the json file
- Get timezone from pytz database https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
- Rename the value of currentCity to whatever defined city name you want to use under the key "cities"
- Open runweathertime.bat, or write "py weathertimeget.py" in a command prompt within the directory containing weathertimeget.py

# Features
- Time will update at local :00 (every minute)
- Weather will update every 11 minutes (This can be changed in the Python script. I might add it as a configurable parameter in settings.json later, but there is a daily API request limit, so 11 minutes should be fine.)

- You may customize the behavior or frequency of weather and time acquisition in the script (schedule.every() ...)\
Read up schedule library docs for more info https://schedule.readthedocs.io/en/stable/
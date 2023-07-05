# Weather python script

This is the **python weather script** that I use personally, https://gitlab.com/thelinuxcast/scripts/-/blob/master/weather.py#modal-confirm-fork-webide. 
This script requires the `requests` module, and an **Openweather** api key, which you need to sign in for in **Openweather**'s website. After getting the key, paste it in the right spot in the script.     

Then go to  [Openweather City](https://openweathermap.org/city), and find the city which you want to know the weather of. So I picked 
lets suppose **New York**. Then after searching for it, and selecting the right city to get info about it.
In the url bar, there will be City number, after this part of link https://openweathermap.org/city/. 
Copy it, paste it after `CITY=`, in between quotations. Then run it, you should get your weather info 
automatically with python, which you can used to make a weather module in polybar.  

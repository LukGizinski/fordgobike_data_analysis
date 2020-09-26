# Ford's GoBike Program Data Exploration
## by Lukasz Gizinski


## Dataset


> I have decided to look into Ford's GoBike Program Data in only spcific months Ocotber 2018 and Ocotber 2019 because I wanted to comapre them and look has there any specific trend change.  
> The data consisted of bike rents and rent details of approximately 360840(Oct 2018 has 180534 of records and Oct 2019 has 180306 of records ) . There is 18 features that describes type of useres, gender, age, time/day of rent. 80513 data points were removed from the analysis due to inconsistencies or missing information.

>In terms of data wrangling steps I have spoted
### Quality issues
    - start time and end time are objects
    - user type, gender and bike_share_for_all_trip can be set to category
    - bike id, start_station_id, end_station_id can be set to object
    - member birth year has dates prior to 1900
### Tidyness 
    - columns_to_drop = ['start_station_latitude', 'start_station_longitude',
                 'end_station_latitude', 'end_station_longitude']
    - drop age outlieres
    
>also I have did Feature Engineering:

    - calculated the age of the user into bins
    - enhanced the dataset with more details about the time like day, hour, weekday
    - there are NaN which I will drop as well thre is enough data


## Summary of Findings

> The bike share system is mainly used during weekdays, the most popular days for bike rides in October 2018 are Monday - Wednesday and Tuesday - Thursday in October 2019. It's intresting change of trend. The system is least  used during weekends.Bikes are mostly used between 7-9 and 16-19 and there's no diffrence between Oct'18 and Oct'19. There is no significant diffrence between Oct 2019 and Oct 2018 in rent duration.There is  diffrence between Oct 18 and Oct 19 - Oct 19 has much more rents by subscribers and less by Customers then Oct 18.There is a increase of bike rents on October 2019 in group of useres with age between 25-30.

>When we add user type(Subscriber/Customer) to the analysis we can observe diffrent behaiviours in bike rents. Customers tend to rent bikes more often during weekends than Subscribers. Both user tupes tend to rent bikes at 8-9am and 5-6pm. Also there is no significant diffrence beteween October 18 and Ocotber 19

>Looks like from both user types males are renting the bikes more often than females and this trend tends to repeat across Subscribers and Customers as well.There's no signifficant diffrence between Oct'18 and Oct'19 there is only more Males bike rents and no change in Females rents since Oct'18.


## Key Insights for Presentation

> Distribution of weekly usage of bike rents
> Distribution of  hourly usage of the bike rent system
> Distribution of bike rents by gender

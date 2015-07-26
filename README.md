# SmileWeather

A library for Search & Parse the weather data from Wunderground conveniently.

![](https://raw.githubusercontent.com/liu044100/SmileWeather/master/SmileWeather-Example/demo_gif/pro_big.png)

#What can it do for you?


##### 1. Handle all complicated things about Search & Parse the weather data.

For example, you can get weather data by using `-(void)getWeatherDataFromLocation:(CLLocation*)location completion:(SmileWeatherDataDownloadCompletion)completion`, in completion block get well formed weather data.

```
    CLLocation *location = [[CLLocation alloc] initWithLatitude:37.322998 longitude:-122.032182];
    [[SmileWeatherDownLoader sharedDownloader] getWeatherDataFromLocation:location completion:^(SmileWeatherData *data, NSError *error) {
        if (!error) {
            //Well formed weather data in here.
        }
    }];
```

You can search place by `-(void)getPlacemarksFromString:(NSString*)string completion:(SmileWeatherPlacemarksCompletion)completion`, it return array of the `CLPlacemark`.

```
[[SmileWeatherDownLoader sharedDownloader] getPlacemarksForSearchDisplayFromString:@"cupertino" completion:^(NSArray *placeMarks, NSError *error) {
        if (!error) {
            //search results: array of placemark in here
        }
    }];
```

![](https://raw.githubusercontent.com/liu044100/SmileWeather/master/SmileWeather-Example/demo_gif/search.png)


##### 2. Need not any weather icon, SmileWeather handle it for you. 

Because by using [climacons font](http://adamwhitcroft.com/climacons/), SmileWeather return the corresponding character that is used for weather icon.

##### 3. Fully localized the related information for almost all the countries in the world.

The Weather information, timestamp, weekday, timezone, etc, localized all the related information as soon as possible.

![](https://raw.githubusercontent.com/liu044100/SmileWeather/master/SmileWeather-Example/demo_gif/localization.png)

# Contributions

* Warmly welcome to submit a pull request.

# Contact

* If you have some advice or find some issue, please contact me.
* Email [me](liu044100@gmail.com)

# Thanks

Thanks for Comyar Zaheri's [Sol° for iOS](https://github.com/comyarzaheri/Sol), I am inspired by this project.

Thanks for [climacons font](http://adamwhitcroft.com/climacons/).

# License

SmileWeather is available under the MIT license. See the LICENSE file for more info.
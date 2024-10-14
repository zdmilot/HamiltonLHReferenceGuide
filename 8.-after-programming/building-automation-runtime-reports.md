# Building Automation Runtime Reports

[Lab Automation Forums](https://labautomation.io/)

## [Automation Report Data](https://labautomation.io/t/automation-report-data/779)

[ScottK](https://labautomation.io/u/ScottK) November 29, 2022, 8:38pm

> Hi all, new here! I was thinking to get everyone’s help brainstorming some ideas for an Automation Report. I am creating a .txt file at the end of our Hamilton Star runs to serve as a summary report of how well the instrument and third party devices ran. It’s meant to be concise and easy to read, something pretty to give users. What do you think are some helpful things to add? The purpose is to have a file to open at the end of the run that has data that will help with troubleshooting if a run fails and give the user confidence the run performed as expected.
>
> So far, I’m thinking to record:
>
> * all temperatures of HHS/CPAC listed at each step
> * Instrument serial name, run ID, version of method, date
> * timestamps of steps
> * list of errors and recoveries
> * User selections
> * list of timers stopped
> * trace log file name
>
> Essentially, what have you found is a really important piece of data to have the instrument record for troubleshooting?



[chips-a-hoai](https://labautomation.io/u/chips-a-hoai) November 29, 2022, 8:58pm

> I usually add reagent barcodes/lot numbers and have moved to SQL databases so that data can easily be parsed.



[bowlineknot](https://labautomation.io/u/bowlineknot) November 29, 2022, 9:53pm

> If you use worklists, the location and name of the worklist selected.
>
> Status of 3rd party devices:\
> ODTC, XPEEL etc.
>
> Records of key variables:\
> Number of samples, timer lengths, wash cycle numbers, etc



[luisvillaautomata](https://labautomation.io/u/luisvillaautomata) November 30, 2022, 2:26am

> I agree with the other suggestions as well.
>
> Also depends on how deep you want to go down this rabbit hole but liquid heights can be good to have if an operator is loading manually made parts, obv the temp and humidity at particular steps as well and not just broadly from some parts.



[Pete](https://labautomation.io/u/Pete) November 30, 2022, 3:32pm

> Capture everything - and only surface only what you need today. You never know what will be valuable down the road. (this is why a db is better)



[ScottK](https://labautomation.io/u/ScottK) November 30, 2022, 7:38pm

> You use SQL databases instead of a report at the end of a run?



[ScottK](https://labautomation.io/u/ScottK) November 30, 2022, 7:38pm

> Didn’t think about the location of the worklist - thanks!



[ScottK](https://labautomation.io/u/ScottK) November 30, 2022, 7:41pm

> That’s a good idea, the temp and humidity along the way. Is there a way a Hamilton can capture humidity and temp or would that just need to be manually done?
>
> Liquid heights would be good, thanks! This is to know if a tube or trough wasn’t filled as high as it needed to be or if a possible offset is off at that location?



[ScottK](https://labautomation.io/u/ScottK) November 30, 2022, 7:43pm

> Good point to capture everything and only surface what you need. I can toggle between modes to do that. For databases, do you find it’s just as fast or is there a lag when using them?



[chips-a-hoai](https://labautomation.io/u/chips-a-hoai) November 30, 2022, 9:11pm

> it’s much easier to query trends and view data between runs versus having to manually comb through all the files in order to get the meta data.



[luisvillaautomata](https://labautomation.io/u/luisvillaautomata) November 30, 2022, 11:16pm

> I don’t know, I usually build my own sensors/devices. It’s way easier now with micropython/circuitpython.
>
> Both. Liquid height is good (remember it’s positional value of Z with Hamilton) so it can allow you to troubleshoot downstream because you can point to this data to say that maybe a manually added component was off.



[Gareth](https://labautomation.io/u/Gareth) December 2, 2022, 9:40am

> I’m not the OP, but querying against a database will generally be quicker than using excel via jet.



[mnewsom](https://labautomation.io/u/mnewsom) December 2, 2022, 6:20pm

> I was actually looking to build a humidity / temp logger for capturing those data. Planned on just grabbing something off adafruit or whatever but curious to hear if there’s one you like.
>
> Outside my wheelhouse but wasn’t sure what kind of accuracy or precision I really needed for this.



[luisvillaautomata](https://labautomation.io/u/luisvillaautomata) December 2, 2022, 7:03pm

> I have most of the reasonably priced sensors available so I’ve made some quick prototypes where I just compare data across lots of sensors. I’m happy to share my code and thoughts. I am also interested in creating something even simpler since I suspect I’ll have to use something like it in my new role to keep an eye on stuff throughout development.
>
> > Outside my wheelhouse but wasn’t sure what kind of accuracy or precision I really needed for this.
>
> I think this is kind of the big question because we may not know what we don’t know because we don’t have the data. Irrespective of accuracy + precision and simply using using it out of the box will allow you to correlate fluctuations with sudden sample failure OR it can allow you trigger different liquid classes in your method for winter/fall when lab conditions can drastically change (seasonal liquid classes).
>
> With lots of these sensors, the accuracy and precision may need adjustment for your calculation (especially true of pressure/gas sensors) BUT I needed a baseline period to determine if there was more than correlation.
>
> Some of the assays were developed well before my time so I wanted to figure out that cutoff. My biggest concern is excessive heating leading to issues that impact the calculations but a lot of boards have that in mind now or you can utilize low power modes so it’s not drawing too much power and constantly heating up.
>
> Are you looking to dump these on a deck? Also in the past I was able to query data with BLE on a [Sensortile](https://www.digikey.com/en/product-highlight/s/stmicroelectronics/sensortile?utm\_adgroup=STMicroelectronics\&utm\_source=google\&utm\_medium=cpc\&utm\_campaign=Dynamic%20Search\_EN\_Focus%20Suppliers\&utm\_term=\&utm\_content=STMicroelectronics\&gclid=Cj0KCQiA4aacBhCUARIsAI55maFoUsrZkiTzUSVH7igFEiIYjhh0XE0e-nZKavn0m01K6HmNyFTLWRAaAlFYEALw\_wcB) which STMicroelectonics has a lot of cool stuff developed for it to help support.
>
> [The Python SDK alone is amazing and the examples are very easy to adjust.](https://github.com/STMicroelectronics/BlueSTSDK\_Python)



[mnewsom](https://labautomation.io/u/mnewsom) December 5, 2022, 2:02pm

> You hit the nail on the head with the seasonal lab conditions. Like you mentioned it’s hard to know what you don’t know, so automating the collection of those data and being able to do post-mortems without relying on people to log the numbers is all I’m looking at currently.
>
> Having a custom liquid class that is used automatically depending on the environmental conditions would be a good feature for v2.
>
> I’ll start a thread about it so we don’t derail this one!



[Kalpesh](https://labautomation.io/u/Kalpesh) December 14, 2022, 2:49am

> Hamilton new S-CAP( hepa filters) have the Temp and humidity meter and it records. you can easily access the data in the method or logs if needed.\
> Other than that Agilent sell some power/Humidity/Temperature sensors, which you can use and collect data and use it later



3 Likes[ScottK](https://labautomation.io/u/ScottK) January 13, 2023, 6:44pm

> > S-CAP( hepa filters)
>
> Can it be used on a Hamilton Star? Do you have a link by chance?



[Kalpesh](https://labautomation.io/u/Kalpesh) January 14, 2023, 2:08am

> Sorry. I dont but i m sure if u ask your Hamilton rep. they can get u more information



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) January 14, 2023, 4:23pm

> We offer our Clean Air Protection (CAP) hoods for the NIMBUS, STAR, and VANTAGE product lines. They are each appropriately named N-CAP, S-CAP, and V-CAP. My understanding is that the N-CAP and S-CAP are the same design with the exception of the hardware integration while the V-CAP has some slight differences to accommodate the VANTAGE platform. All have the same feature/function set though.
>
> As Kalepsh recommended, please get in touch with your local Hamilton rep for more info. Feel free to message me directly if you need the contact info!




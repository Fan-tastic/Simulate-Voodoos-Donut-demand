This is about the Simulate Voodoo's Donut Demand assignment.

Firstly I defined all the locations and added properties to each of them

For example:
var Downtown={
        HoursOfOperation : 11,//from 7a-6p, operation hour is 11
        HourlyFootTraffic : Math.floor(Math.random() * 141 + 80),  //randomize a number from hourly foot traffic range
        PercentEntering : 0.1,
        NumberOfDonutsOrderdPerEnt:4
   }; 

   For the var HoursOfOperation, it is from 7am-5am, which is 11 hours;
   For the var HourlyFootTraffic, it will be a random number from a certain range, I put "Math.random()"on it and make sure the number output from this range. 
   Both vars HourlyFootTraffic and PercentEntering may have decimal numbers, I put a "Math.floor" to make them integers.

   Secondly, I was told that Hourly foot traffic should be randomly selected from the range provided, for each hour of the day, which means I should not just multiple the HoursOfOperation by NumberOFDonutsForEveryHour, I have to add a for loop and make a random sum to output the TotalNumbersOfDonutsForWholeDay.
   Here it is:
   for(i=0;i<12;i++) {
        NumberOFDonutsForEveryHour1 = Math.floor(Downtown.HourlyFootTraffic * (Downtown.PercentEntering) * Downtown.NumberOfDonutsOrderdPerEnt);
        TotalNumbersOfDonutsForWholeDay1 = i * NumberOFDonutsForEveryHour1;
    }

    Lastly, output both NumberOFDonutsForEveryHour and TotalNumbersOfDonutsForWholeDay.

    
    One test result (for the first two locations):
    
Number Of Donuts For Every Hour in Downtown is 76
Total Numbers Of Donuts For Whole Day in Downtown is 836
57 Number Of Donuts For Every Hour in CaptitolHill is 9
Total Numbers Of Donuts For Whole Day in CaptitolHill is 108
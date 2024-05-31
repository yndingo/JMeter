<p align="center">
  <b>Load test for search engine Rambler</b>
</p>

<b>Actions</b>
1. open main page with getting all context
2. search by random phrase from Maknamara_Ye._Malenkiyi_Cvetochnyiyi_Ma.csv
3. select random link and follow by it
4. print to log title of the opened page and all absolute hyperlinks available on the page
5. after each action must be random delay (1-5sec)

<b>Load test</b>

I have calculated such results:
1. pacing 180 sec
2. each ramp 3 users of total 5 ramps
3. duration of each ramp is 5 minutes
4. ramp up and down set 0
5. constant throughput timer is 0.3

I have decided to low load data, cause not to be blocked in suspicion of DDOS

<b>Results</b>

So i can make such resolutions by the results:
1. 156 seconds is average time of whole trasaction
2. 145 samples are done in the test
3. average time of sample is 53 seconds
4. about 2% errors were detected (NoHTTPResponse,ResourseNotFound)
5. During test we can see that responses are growing the main reason is that my internet channel width is prerry low at that moment 

[Test report. All requests](Test_Results/rambler_report.csv)

[Test report. All errors](Test_Results/rambler_errors.xml)

![Aggregate Report](Test_Results/1.aggregate_report.png?raw=true "Title")

Here we can see how many transactions per second are done in lapse of time
![Transactions per second](Test_Results/2.transactions_per_second.png?raw=true "Title")

Here we can see responses in lapse of time
![Response times over time](Test_Results/3.response_times_over_time.png?raw=true "Title")

Here we can see active users in lapse of time
![Active threads over time](Test_Results/4.active_threads_over_time.png?raw=true "Title")


<p align="center">
  <b>Load test for altenar service</b>
</p>

<b>Actions</b>
1. open API GetUpcoming
2. select 5 events where SelectionsCount > 10
3. open API GetEventDetails with EventId = random event from step #2
4. load ramps 1 => +2 => +5 => +10, each ramp works per 20 sec

description REST API service SB2 by Swagger specification 
[feApiSwaggerSpec.json](Test_Data/feApiSwaggerSpec.json)

<b>Load test</b>

I have calculated such results:
1. pacing 0 sec
2. load ramps 1 => +2 => +5 => +10, each ramp works per 20 sec

![Test plan](Test_Results/1.test_plan.png?raw=true "Test plan")

<b>Results</b>

So i can make such resolutions by the results:
1. no errors
2. GetUpcoming 90%% 299ms
3. GetEventDetails 90%% 288ms
4. no max perfomance found
5. tested api works stable on this ramps




Here we can see how many transactions per second are done in lapse of time
![Transactions per second](Test_Results/4.results_Transactions_per_Second.png?raw=true "Transactions per second")

Here we can see responses in lapse of time
![Response times over time](Test_Results/3.results_Response_Times_Over_Time.png?raw=true "Response times over time")

Here we can see active users in lapse of time
![Active threads over time](Test_Results/2.results_Active_Threads_Over_Time.png?raw=true "Active threads over time")


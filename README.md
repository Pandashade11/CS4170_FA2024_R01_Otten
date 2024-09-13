1.) Some examples of parallel operations in my daily life include:
    -Shopping lanes:
        This example that we used in class would be classified as data parallelism. In this example, the more checkout lines that are available, the more customers can check out at once, making sure everything runs smoothly 
        with a line. This design optimizes customer wait times by reducing the time the customer has to wait to check out. 
        Speedup Calculation: Say there is one checkout lane, and there are 10 people with an average checkout time of 6 minutes per person. Our serial time, in this case, would be 60 minutes. Say we were to add five checkout
        lanes. Now, it only takes 12 minutes to go through that same line. S=Ts/Tp, S = 60/12; S=5. In this case, our speedup would be 5x.
    -Making Dinner:
        This example would be classified as task parallelism. For this example, let's say you are making a pasta dinner; you need to put your garlic bread in the oven, make your pasta, make your sauce, and do the dishes.
        To add parallelism to this example, you would need to simulate doing these tasks at once instead of waiting for your pasta to be done before you start your sauce or put the garlic bread in the oven. 
        Speedup Calculation: For ease of calculation, let's say each task will take 15 minutes a piece. Four tasks will take you an hour to make dinner, so your total serial time will be an hour. Now, if you were to parallelize
        this, you would do all of these tasks simultaneously except the dishes because you have to wait until you're finished with dinner, so that part will stay serial. Instead of our dinner taking an hour now, it will only take
        30 minutes. S=Ts/Tp; S=60/30; S=2. In this case, our speedup would be 2x.

2.) My Desktop computer has a new gen CPU and GPU capable of computing at high speeds across multiple cores and threads, meaning the theoretical parallel processing power of my computer will be much greater than its serial
processing power. A cell phone, on the other hand, would have much lower theoretical parallel and serial processing power due to its lack of GPU and a much smaller and more limited CPU. Some parallel hardware in my computer 
includes my GPU, which has thousands of cores that can carry out tasks in a parallel fashion, as well as a multi-core CPU, which is designed to assign tasks across its multiple cores and threads. More hardware might include 
high-speed RAM, which can help decrease the memory bottleneck found in parallel programming.

3.),
  1.)Task parallelism would work best in this case because the computer has 16 cores. We can assign each image to its own core, allowing for 16 images to be processed simultaneously. Our serial time for this would be calculated 
as 1,000 images * 10 minutes per image = 10,000 minutes/60 minutes = 166.67 hours; this will not fit the user's daily requirement needs, so we must parallelize it. We can split one image per core, so in theory, we should be 
16x more efficient, 1,000 images / 16 cores = 62.5 processes * 10 min = 625 minutes or just under ten and a half hours. This would be an efficient way to ensure the user completes the daily image processing requirements.
  2.)If we were to 10x this workload, 10,000 images / 16 cores = 625 processes * 10 minutes = 6,250 minutes or a little over 4 days. This will take too long for the user, so it will no longer work. We can split up the processes by adding
nodes to decrease our computing time as long as the memory allows. To do this, we can compute ten items for each node so that all 10,000 images are processed daily with plenty of time left over.  

4.)
  1.) Tasks that might be assigned to specific faculty members might include things like party prep, getting food, making a playlist, inviting people, cleaning, and providing entertainment. Say we have six members planning the party; we 
can split up each task so that one member gets one task to complete so person one can prep, and person two can get food... This displays data parallelizm by not one person doing all of the work and splitting the workload among the group. 
  2.) We can add data parallelism to this part of the task by splitting up the house into different subsections and having one member work on cleaning that specific part of the house. This approach would split the work amongst
the group so everyone would actively clean up a part of the house until it was done. One problem we might run into is the availability of cleaning supplies; for example, if someone is vacuuming the living room and the person doing the bathroom
is finished and just needs to vacuum to be done, they will be bottlenecked. They cannot finish until the person is finished in the living room. To fix this problem, instead of dividing up the house, we can just split the group by 
tasks, so one person does all of the vacuuming, and one person does all of the mopping... 
  3.) To combine task and data parallelism to the party, we could assign one person per primary task, like in the first part, but then have a bunch of subsections that we assign everyone to complete. For example, say we assign member 1 to 
get the food; we can assign person 1 to plan the food; person 2 gathers the food, person 3 gets the drinks, and person 4 gets the plates and napkins... Then, when it finally comes to the party, the person assigned to the primary task is 
responsible for making sure everything is ready when it's actually party time. 

# ASSIGNMENT: Sampling and Reproducibility in Python

Read the blog post [Contact tracing can give a biased sample of COVID-19 cases](https://andrewwhitby.com/2020/11/24/contact-tracing-biased/) by Andrew Whitby to understand the context and motivation behind the simulation model we will be examining.

Examine the code in `whitby_covid_tracing.py`. Identify all stages at which sampling is occurring in the model. Describe in words the sampling procedure, referencing the functions used, sample size, sampling frame, any underlying distributions involved, and how these relate to the procedure outlined in the blog post.

Run the Python script file called whitby_covid_tracing.py as is and compare the results to the graphs in the original blog post. Does this code appear to reproduce the graphs from the original blog post?

Modify the number of repetitions in the simulation to 100 (from the original 1000). Run the script multiple times and observe the outputted graphs. Comment on the reproducibility of the results.

Alter the code so that it is reproducible. Describe the changes you made to the code and how they affected the reproducibility of the script file. The output does not need to match Whitby’s original blogpost/graphs, it just needs to produce the same output when run multiple times

# Author: Ethan Ross

```
1. Sampling

There are two places in the code where sampling occurs.

Sample #1: Infecting Step.

    - Procedure: The choice method is used to select 100 random indices. This is a simple random sample.
    - Frame: The entire population.
    - Sample size: 100 people.

This resembles the first suggestion of the article where 10% of the population is to be infected. The article also suggests giving each person a 10% chance of being infected to introduce some randomness and this is not done in the code.

Sampling #2: First contact tracing.

    - Procedure: A simple random sample of all infected people is collected, and the units in the sample will then be successfully traced. This is achieved by generating 100 random numbers between 0 and 1 using the .rand method. If a particular infected person's number is less than the threshhold of 0.2, then their 'traced' value is set to true, indicating that they were successfully traced.
    - Frame: The 100 infected people
    - Sample Size: Can be computed by running len(ppl.loc[ppl['traced']]) before the secondary contact tracing. Will be approximately 20 individuals. Re-running the code many times produces numbers around that point.

This matches the strategy from the article as each of the random numbers generated has a 20% chance of being smaller than 0.2, hence each infected person has an only 20% chance of being successfully traced.

Sampling #3: Second contact tracing.

    - Procedure: If more than one infected person can be traced back to a single event, then all infected people at that event are successfully traced. This is achieved by first counting how many infected people attended a brunch and how many infected attended a wedding, making use of the value_counts() method. We then produce list of the events where more than two infected persons are associated to it. Finally, using the .isin() method, if any infected person is in one of these special events with more than one trace, then all infected persons at that event are considered traced.
    - Frame: All infected people who have attended events.
    - Sample size: Can be computed by running len(ppl.loc[ppl['traced']]) and subtracting the sample size from the first contact tracing. Will almost always be around 80 people, sometimes dropping to around 60 if at most one person was successfully traced to a wedding in the first contact tracing.


2. Comparison To Blog Post

The code reflects the procedure in the blog post in spirit, but differs in one key aspect. In the article, there are two distinct weddings and 80 distinct brunches. And yet, the code one distinguishes between 'wedding' and 'brunch' and so, in effect, this code is based on the assumption of there being 1 large wedding with 200 attendees and a GARGANTUAN brunch of 800 people (only the most charismatic of drag queens could possibly achieve such a feat). This means that around 80% of all infected people will be successfully traced in the second step as it is very unlikely that in our random initial sampling we will only infect one person who attended a brunch. 

Indeed, if we look at the graph produced by the code, we see that the proportion of successfully traced infected units tied to weddings hovers around 0.2 which is approximately what the true proportion of infected people who attended weddings. This is very much unlike the blog post where there is a large spread towards numbers larger than 0.2. Again, this is to be expected as the python file is making very different assumptions than the blog post.

3. Reproducibility


The code as presented is not reproducable as the two steps of random selection--who will be infected and which infected people will be successfully contact traced--are not pre-seeded.

4. Alterations To Ensure Reproducibility

I replaced the dummy variable in the definition of the simulation by an integer variable random_state (with default value being 0). How I used this to make the code reproducable was by adding the following line at the beginning of the definition of the simulation function.

# Using random_state to generate a random seed.
  np.random.seed(random_state)

Now when the 100 simulations are run, each of the integers between 0 and 100 being inputted into the simulation function are 100 distinct random seeds for 100 different simulations. However, since we are always calling upon the same set of seeds, the result is then reproducable.



```


## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Altercation of the code|The code changes made, made it reproducible.|The code is still not reproducible.|
|Description of changes|The author explained the reasonings for the changes made well.|The author did not explain the reasonings for the changes made well.|

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 09/04/2025`
* The branch name for your repo should be: `assignment-1`
* What to submit for this assignment:
    * This markdown file (a1_sampling_and_reproducibility.md) should be populated.
    * The `whitby_covid_tracing.py` should be changed.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-1`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.

# Assignment 1: Design a Logical Model

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).

ERD attached to assignment.

## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.

 Added to ERD
## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

Architecture 1 is type 1 and Architecture 2 is type 2. Type 2 retains old customer address while Type 1 overwrites it.

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Privacy Implications
There are potential privacy implications when retaining customer address history, especially for Type 2:

If the data is mishandled, exposed, or used inappropriately. For instance, outdated addresses might expose sensitive past information such as previous residences.

Depending on the jurisdiction, storing historical addresses may require compliance with privacy regulations like GDPR or CCPA. These regulations give users the right to request deletion or access to their personal data, including past addresses.

Privacy laws often encourage businesses to follow the principle of data minimization—storing only the data necessary for operational purposes. Retaining multiple historical addresses unless there’s a clear business justification (e.g., for fraud prevention, auditing) might be seen as excessive.

In light of privacy considerations, it’s important to assess the need for storing historical address data. Type 1 (overwriting addresses) might be preferable for minimizing privacy risks unless there’s a clear operational need to track address history, in which case proper security measures should be implemented for Type 2.
```

## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
The Adventtureworks Schema is more elaborate than my ERD. 

The Adventureworks Schema divides the tables in color codes and I may want to change that in my ERD
```

# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `September 28, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-4-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.

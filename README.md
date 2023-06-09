<h2>Project description</h2><div class="paragraph">You work as an analyst for the telecom operator Megaline. The company offers its clients two prepaid plans, Surf and Ultimate. The commercial department wants to know which of the plans brings in more revenue in order to adjust the advertising budget. </div><div class="paragraph">You are going to carry out a preliminary analysis of the plans based on a relatively small client selection. You'll have the data on 500 Megaline clients: who the clients are, where they're from, which plan they use, and the number of calls they made and text messages they sent in 2018. Your job is to analyze clients' behavior and determine which prepaid plan brings in more revenue. </div><h3>Description of the plans</h3><div class="paragraph">Note: Megaline rounds seconds up to minutes, and megabytes to gigabytes. For <strong>calls</strong>, each individual call is rounded up: even if the call lasted just one second, it will be counted as one minute. For <strong>web traffic</strong>, individual web sessions are not rounded up. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.</div><div class="paragraph paragraph_has-one-child"><strong>Surf</strong></div><ol start="1"><li>Monthly charge: $20</li><li>500 monthly minutes, 50 texts, and 15 GB of data</li><li>After exceeding the package limits:
 <ul><li>1 minute: 3 cents</li><li>1 text message: 3 cents</li><li>1 GB of data: $10</li></ul></li></ol><div class="paragraph paragraph_has-one-child"><strong>Ultimate</strong></div><ol start="1"><li>Monthly charge: $70</li><li>3000 monthly minutes, 1000 text messages, and 30 GB of data</li><li>After exceeding the package limits:
 <ul><li>1 minute: 1 cent</li><li>1 text message: 1 cent</li><li>1 GB of data: $7</li></ul></li></ol><h3>Instructions on completing the project</h3><div class="paragraph"><strong>Step 1</strong>. <strong>Open the data file and study the general information</strong></div><div class="paragraph">File path: </div><div class="paragraph"><em>/datasets/megaline_calls.csv</em> <a href="https://practicum-content.s3.us-west-1.amazonaws.com/datasets/megaline_calls.csv">Download dataset</a></div><div class="paragraph"><em>/datasets/megaline_internet.csv</em> <a href="https://practicum-content.s3.us-west-1.amazonaws.com/datasets/megaline_internet.csv">Download dataset</a></div><div class="paragraph"><em>/datasets/megaline_messages.csv</em> <a href="https://practicum-content.s3.us-west-1.amazonaws.com/datasets/megaline_messages.csv">Download dataset</a></div><div class="paragraph"><em>/datasets/megaline_plans.csv</em> <a href="https://practicum-content.s3.us-west-1.amazonaws.com/datasets/megaline_plans.csv">Download dataset</a></div><div class="paragraph"><em>/datasets/megaline_users.csv</em> <a href="https://practicum-content.s3.us-west-1.amazonaws.com/datasets/megaline_users.csv">Download dataset</a></div><div class="paragraph paragraph_has-one-child"><strong>Step 2. Prepare the data</strong></div><ul><li>Convert the data to the necessary types</li><li>Find and eliminate errors in the data</li></ul><div class="paragraph">Explain what errors you found and how you removed them. </div><div class="paragraph">For each user, find:</div><ul><li>The number of calls made and minutes used per month</li><li>The number of text messages sent per month</li><li>The volume of data per month</li><li>The monthly revenue from each user (subtract the free package limit from the total number of calls, text messages, and data; multiply the result by the calling plan value; add the monthly charge depending on the calling plan)</li></ul><div class="paragraph paragraph_has-one-child"><strong>Step 3. Analyze the data</strong></div><div class="paragraph">Describe the customers' behavior. Find the minutes, texts, and volume of data the users of each plan require per month. Calculate the mean, variance, and standard deviation. Plot histograms. Describe the distributions. </div><div class="paragraph paragraph_has-one-child"><strong>Step 4. Test the hypotheses</strong></div><ul><li>The average revenue from users of Ultimate and Surf calling plans differs.</li><li>The average revenue from users in NY-NJ area is different from that of the users from other regions.</li></ul><div class="paragraph">You decide what alpha value to use.</div><div class="paragraph">Explain:</div><ul><li>How you formulated the null and alternative hypotheses.</li><li>What criterion you used to test the hypotheses and why.</li></ul><div class="paragraph paragraph_has-one-child"><strong>Step 5. Write an overall conclusion</strong></div><div class="paragraph"><strong>Format:</strong> Complete the task in Jupyter Notebook. Put the programming code in <code class="code-inline code-inline_theme_light">code</code> cells and text explanations in <code class="code-inline code-inline_theme_light">markdown</code> cells, then apply formatting and headings.</div><h3>Description of the data</h3><div class="paragraph">Remember! Megaline rounds seconds up to minutes, and megabytes to gigabytes. For <strong>calls</strong>, each individual call is rounded up: even if the call lasted just one second, it will be counted as one minute. For <strong>web traffic</strong>, individual web sessions are not rounded up. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.</div><div class="paragraph">The <code class="code-inline code-inline_theme_light">users</code> table (data on users):</div><ul><li><em>user_id</em> — unique user identifier</li><li><em>first_name</em> — user's name</li><li><em>last_name</em> — user's last name</li><li><em>age</em> — user's age (years)</li><li><em>reg_date</em> — subscription date (dd, mm, yy)</li><li><em>churn_date</em> — the date the user stopped using the service (if the value is missing, the calling plan was being used when this database was extracted)</li><li><em>city</em> — user's city of residence</li><li><em>plan</em> — calling plan name</li></ul><div class="paragraph">The <code class="code-inline code-inline_theme_light">calls</code> table (data on calls):</div><ul><li><em>id</em> — unique call identifier</li><li><em>call_date</em> — call date</li><li><em>duration</em> — call duration (in minutes)</li><li><em>user_id</em> — the identifier of the user making the call</li></ul><div class="paragraph">The <code class="code-inline code-inline_theme_light">messages</code> table (data on texts):</div><ul><li><em>id</em> — unique text message identifier</li><li><em>message_date</em> — text message date</li><li><em>user_id</em> — the identifier of the user sending the text</li></ul><div class="paragraph">The <code class="code-inline code-inline_theme_light">internet</code> table (data on web sessions):</div><ul><li><em>id</em> — unique session identifier</li><li><em>mb_used</em> —  the volume of data spent during the session (in megabytes)</li><li><em>session_date</em> — web session date</li><li><em>user_id</em> — user identifier</li></ul><div class="paragraph">The <code class="code-inline code-inline_theme_light">plans</code> table (data on the plans):</div><ul><li><em>plan_name</em> — calling plan name</li><li><em>usd_monthly_fee</em> — monthly charge in US dollars</li><li><em>minutes_included</em> — monthly minute allowance</li><li><em>messages_included</em> — monthly text allowance</li><li><em>mb_per_month_included</em> — data volume allowance (in megabytes)</li><li><em>usd_per_minute</em> — price per minute after exceeding the package limits (e.g., if the package includes 100 minutes, the 101st minute will be charged)</li><li><em>usd_per_message</em> — price per text after exceeding the package limits</li><li><em>usd_per_gb</em> — price per extra gigabyte of data after exceeding the package limits (1 GB = 1024 megabytes)</li></ul><h2>How will my project be evaluated?</h2><div class="paragraph">We’ve put together some project assessment criteria. Read over them carefully before you get to work.</div><div class="paragraph">Here’s what project reviewers will look at when assessing your project:</div><ul><li>How you explain the problems identified in the data</li><li>How you prepare the data for analysis</li><li>What graphs you plot for distributions</li><li>How you interpret the resulting graphs</li><li>How you calculate the standard deviation and variance</li><li>Whether you formulate the alternative and null hypotheses</li><li>What methods you use to test hypotheses</li><li>Whether you interpret the results of your hypothesis tests</li><li>Whether you follow the project structure and keep the code tidy</li><li>The conclusions you come to</li><li>Whether you leave comments at each step</li></ul><div class="paragraph">Our <a href="https://datapracticum.gatsbyjs.io" target="_blank">Knowledge Base</a> has everything that you’ll need in order to complete the project.</div><div class="paragraph">In the video below, we cover some of the common stumbling blocks in completing this project.</div><div class="paragraph paragraph_has-one-child"><div class="iframe-wrapper"><iframe allowfullscreen="" src="https://www.youtube.com/embed/MHxU_8d2dGk"></iframe></div></div><div class="paragraph">Good luck!</div></div>

**Metric Experience PRD for Claude Code**

**Product Team Goals of the metric experience and where we need to be:** 

* Drive Metric adoption to 15K MAU this year  
* The metric stands on its own as a clear, trustworthy unit of analysis  
*  It’s immediately obvious to a user what’s happening and whether it matters  
* Standardization in actions a user can take  
* There is flexibility in what is presented to the user (e.g., which insights are presented, how much/little info is included. etc.)

**Problems to Solve**

1. **Business User metric discoverability and actionability**   
   1. Business users aren’t able to discover relevant metrics without analysts sharing them in dashboards or slack canvases today.   
   2. Business users on web or mobile have to browse and follow a metric. Can they discover metric card, quick filters and breakdowns when asking a question in slackbot?   
   3. Can metric cards have clear CTAs based on the surface, focused on personalization/collaboration and ways to get to deeper analysis?   
      1. Slack : follow metric, create alert, add to a brief, ask agent  
      2. Web : follow metric, create alert, explore metric 						  
2. **Business User metric understanding**  
   1. There is confusion when the metric is aggregated (cumulative/non-cumulative). 	  
      1. Customers and internal stakeholders consistently report confusion and functional gaps around how cumulative vs. non-cumulative metrics are displayed on the **Metric Details Page (Explore Metric)** and **Metric Card (BAN)**. The core issues cluster into three pain points:  
1. **BAN always shows cumulative aggregation** regardless of how the metric is defined — even when users set a metric to non-cumulative, the top-level value is the sum of the full period, not the period-specific value.  
2. **No user-facing toggle** to switch between cumulative and non-cumulative views.  
3. **Data confusion for non-cumulative metric types** (averages, rates, point-in-time values) where aggregating over time produces incorrect or misleading results.							  
3. **Analyst metric discoverability and actionability** 			  
   1. Analysts aren’t able to quickly create metrics when building a dashboard (they have to navigate into D360)  
   2. Analysts are copying URL links to paste metrics, visualizations and dashboards into a slack canvas today. How can this be more discoverable?												

**Proposed Solution (need to test/validate)**

1. **Metric Discoverability and actionability for Business User** \- create a way to discover/follow metrics and show breakdowns (contributors or drivers) when asking questions in slackbot:	  
   1. **Discover/Follow metrics & add to brief flow**   
      1. Show metric card in slackbot when business user is asking a question that is related to the metric   
      2. Business user can follow metric and this goes to “My metrics” list tab within Slackbot   
      3. Business user discovers that this metric is relevant and adds this metric to the Inspector brief (which is a scheduled brief/analysis of metrics an Analyst configured)  
      4. Follow metric → adds to My Metrics tab (persistent, on-demand, in Slackbot)   
      5. Add to brief → optional additional action to include metric in scheduled brief DM These are complementary, not competing. My Metrics tab is the primary destination. Brief is the proactive push surface.  
      6. Business user can also create alert   
           
   2. **Quick Filter and Breakdown interaction model:**   
      1. The default state is Trend. Contributors and Drivers show a horizontal bar breakdown by Segment. Trend shows a sparkline with a goal line. No carousel.										  
2. **Metric Understanding**   
   1. As a business user, I want the Metric Card BAN to show a tooltip with the full underlying value, so that I can understand the complete metric value when the number is abbreviated.   
   2. As a business user, I want the Metric Details Page to display the correct (non-cumulative) value as the headline number, so that I'm not shown a misleading cumulative sum when the metric is defined as non-cumulative.   
   3. As a business user, I can see the aggregation type (cumulative or non-cumulative) set by an analyst on the metric card and metric details page. 		  
      1. Show aggregation type as a label on the metric card and metric details page: \- Cumulative metric → badge: "Cumulative" \- Non-cumulative metric → badge: "Non-cumulative" Badge appears below the metric name in the collapsed card header.  
      2. Cumulative is running total, non-cumulative shows the value for each period. 										  
3. **Metric Publishing for Analyst**   
   1. create metric within a dashboard   
   2. create action ‘publish to slack canvas’ on a metric, visualization or dashboard so that analysts can easily share the insights into an existing canvas or new canvas. 

**User Journey Flow**

* Jordan (Enterprise AE) is working on building pipeline   
  * Discovers, follows and manages relevant metrics in slackbot. Can also add them to the Inspector brief to personalize the metrics on the brief. 	  
  * Understands how the metric value is calculated/aggregated  
  * View breakdowns (contributors/drivers) of the metric  									  
* Maya (Sales Analyst) is supporting Enterprise Sales Team  
  * Builds dashboards, visualizations and metrics and publishes to Slack canvas ~~shared in the Enterprise sales slack channel and canvas.~~ 	  
  * Maya is able to create metric within a dashboard 				
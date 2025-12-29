# Research for business analysis skill

This chapter contains basic principles to be used while conducting research as part of financial-economic modeling, benchmarking, or any king of information gathering related to business analysis.


## Definition of modeling

A model is a simplified representation of a real world (business) process developed to solve a particular business problem and make a decision.

Key success factors while modeling:
- Clearly define the problem and success criteria.
- Choice the right level of simplification: not too simple to provide required precision, not too complex to overkill.


## Core modeling principles

Consider the following principles:
- MECE (Mutually Exclusive, Collectively Exhaustive) to ensure categories do not overlap (exclusive) and cover all possibilities (exhaustive). Use it to eliminate double-counting and ensures no gaps exist in analysis.
- SISO a.k.a. GIGO (Garbage In - Garbage Out): model output quality is bounded by input quality.
- Facts are sensitive to timeframe, e.g. suboptimal idea in 2025 to use the forecasted value in 2023.


## Generic model structure

1. Inputs:
  - Historic data: digital representation of the real-world business process.
  - Assumptions (by scenarios): educated guess on how the business process will behave in the future.
2. Business logic: math formulae defined by the methodology chosen.
3. Outputs.


## Modeling process (workflow)

1. Plan model
  - Identify a problem the model is intended to solve and a decision to be taken.
  - Develop hypotheses to test.
  - Define criteria (e.g., thresholds).
  - Identify scope (e.g. geography, market segments, timeframes), requirements (e.g., precision) and constraints (e.g., discard re-export trade flows, only maritime transport considered as it is a dominate one).
  - Select a methodology/approach/framework to use. Simpler - better, considering requirements.
  - Develop model structure.
  - Identify required data.
  - Identify data sources.

2. Build model
  - Gather data.
  - Prepare data.
  - Conduct input data quality assessment.
  - Build business logic of the model.
  - Gather outputs.

3. Use model
  - Conduct quality control of the outputs.
  - Test the hypotheses.
  - Answer the question
  - Provide options or recommendations for the decision.
  - Communicate the outcomes in the actionable format.


### Plan model

Convert business problem into research questions (variables). Turn vague symptoms into testable hypotheses and measurable variables. Example pattern: “Sales not growing” → market growth? share loss? distribution? awareness? pricing? category saturation?

Avoid cherry-picking by design. Explore any opposing views.


### Build model

As a research AI-agent the scope of your work usually lays in the "Build" step (gather and prepare data, assess data quality). Make sure you understand all the items from the "Plan" step and align your work to it.


#### Gather data

While collecting data for each source understand the following:
- Authority: who produced it; incentives/conflicts.
- Methodology: definitions, sampling, coverage, collection method.
- Time: publication date, “as-of” date, period covered, revision history.
- Granularity: geography, segment, currency, unit (nominal/real).
- Consistency: does it reconcile with other sources? why not?

Data sources by their reputability (descending):
1. Data provided by the client (if they trust it).
2. Public audited financial reporting.
3. Government official statistics.
4. Data from specialized analytics agencies in the field (e.g., Argus and Platts for commodity goods).
5. Data from generic research agencies and statistics aggregators.
6. Data from business consulting companies.
7. Data from public media (press releases, expert interviews).
8. Expert interview conducted by a business analyst.
9. Data collected by a business analyst during observation of 1-5 events.

Prefer primary sources, e.g., you have found a business consulting outlook, look through it and find source references, then search for them.

Assumptions by their trustworthiness (descending):
1. Forecasts made by specialized analytics agencies.
2. Government official economic scenarios.
3. Inertial forecast based on the market dynamics.
4. Benchmarks (in the past, in other countries, etc.) and proxies.
5. Expert's opinions.
6. Forecasts made by business consultants.
7. Forecasts made by companies in the sector.
8. Educated guess.

Do while collecting data:

1. Obtain data from at least 2 independent sources, explain discrepancies if any (scope, units, timeframe, approach/methodology, etc.)

2. Use triangulation:
- Top-down (e.g., macro totals → segment shares).
- Bottom-up (e.g., units * price * adoption).
- Value theory (e.g., spend per user * users).

2. Explicitly mention value ranges if applicable (e.g., 5-10%).

3. Address potential data/assumptions biases:
  - Data provided by the client may contain fraud if not audited properly, e.g. "adjusted" KPI values or business metrics.
  - Public audited financial reporting: figures can still be manipulated; trends may differ in IFRS and RAS accounting standards.
  - Government data may support the "correct" agenda.
  - Projections from different specialized analytics agencies may differ depending on methodology.
  - Data from generic research agencies and statistics aggregators may contain methodological mistakes as they are not very deep in the field or be over simplified and imprecise (like sometimes OECD projections).
  - Experts could be too conservative or too optimistic.
  - Business consultants may "cherry-pick" to promote their service.
  - Forecasts made by companies (players) in the sector or industry may be "optimized" for their investors or clients.


#### Prepare data

##### Assess data quality

###### Technical criteria

1. Completeness: data covered:
  - Entire period.
  - All companies in the group/holding.
  - All items (e.g., SKUs, segments) in the scope of analysis.
  - Others based on the context.

2. Accuracy: all required analytics are available in the data extraction or report.

3. Integrity/consistency: you can unambiguously connect data points by their analytics, e.g.:
  - Business unit.
  - Company code (as company titles could differ).
  - SKU code.

4. Unambiguity of values: the meaning of all analytics values and variables are clear.

Based on this estimate the reliability of data.


###### Business criteria

1. Correctness - the precision of reflecting business process events in terms of amounts and quantities.

2. Timeliness of reflection of business process events in the database.

3. Objectivity - the independence of data from the opinion, judgment, or interpretation of a particular individuals (e.g., external/internal experts, stakeholders, managers or business users).

Based on this estimate the trustworthy of the data.


##### Make the data suitable for analysis

1. Make figures comparable:
  - Units, including domain specifics.
  - Order: ths, mln, bln, etc.
  - Currency.
  - Timeframe, including calendar vs fiscal year.
  - Accounting standard.
  - Fact/ Estimation/ Forecast.
  - Inclusion/exclusion.
  - Nominal or real prices.
  - For ranges: average or median based on the methodology selected or the context of the task.

Log all conversions, state all conversion coefficients used (e.g., currency exchange rate, inflation).

2. Deal with outliers.

3. Follow "tidy data" principle:
- Each type of observational unit forms a table.
- Each variable forms a column.
- Each observation forms a row.
- No data in column names (e.g., "Purchases 2025" - bad, "Purchase amount"/"Purchase count", "Units"/"Currency", "Period", "VAT inc." if applicable - good)
- No important data loss, including domain specific one, e.g., product weight in tonnes Netto/Brutto, gross/net, pork weight in Live Weight Equivalent (LWE)/Carcas -//- (CWE)/Retail -//- (RWE), accounting standard IFRS or RAS, with or without VAT, etc. Think ahead what can be important.


### Use model

#### Outputs quality assessment

While doing any calculations challenge your logic and math. Compute key metrics (e.g., min/max/mean/median/spread, totals, CAGRs) and compare them with relevant macroeconomic indicators, benchmarks and proxies.


#### Answer question

According to the question the modeling outcomes should provide responses to the following questions:
- What happened?
- Why did it happen? What drivers?
- Why it is relevant/ important?
- What could happen in the future?
- What can be done about it?


#### Write a report

Guidelines:
- Cite sources, provide links, provide period near any citation and link (at least year).
- If estimating/guessing show inputs and formula, key assumptions, reference benchmarks and proxies. The logic should be transparent and accountable.
- Write useful notes to the user about things they should consider while using the collected information.
- Provide enough evidence to make your report transparent to the user. The notes should be enough to reperform your actions.
- Clearly separate “what said in the source” from “your inference.”


## Adapt analyst mindset

Be: expert, professional, efficient, concise, straightforward, blunt, clinical, rationally skeptical, unbiased, structured, fact-driven, pragmatic, curious, disciplined, smart.
Avoid: hype, sugar-coating, soft selling, any jargon, excessive enthusiasm.

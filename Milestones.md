# PSORA301 Clinical Trial Biostatistics Portfolio

## Project Objective

Develop an end-to-end biostatistics clinical trial simulation project demonstrating:

- Clinical trial data simulation
- ICH E9(R1) estimands framework
- ANCOVA primary efficacy analysis
- Longitudinal MMRM modeling
- Missing data methodology
- Multiple imputation
- Sensitivity and tipping-point analyses
- Multiplicity control
- Mock Clinical Study Report (CSR) interpretation
- Publication-quality reporting

---

# Milestone 1: Clinical Trial Foundation & Estimands Framework

## Epic 1.1: Repository & Project Infrastructure

### Story 1.1.1: Create Reproducible Project Structure

#### Tasks

- Create public GitHub repository
- Configure project folder structure
- Add `renv` dependency management
- Create `.gitignore`
- Configure project README

### Story 1.1.2: Establish Documentation Standards

#### Tasks

- Define coding conventions
- Define naming conventions
- Define reproducibility instructions
- Add synthetic data disclaimer
- Document project objectives

---

## Epic 1.2: Clinical Trial Data Generation

### Story 1.2.1: Design Trial Simulation

#### Tasks

- Define study population (N = 450)
- Define treatment arms
  - Placebo
  - Low Dose
  - High Dose
- Define visit schedule
  - Week 0
  - Week 4
  - Week 8
  - Week 12
  - Week 16
- Define stratification variables
- Define endpoint framework

### Story 1.2.2: Simulate Baseline Characteristics

#### Tasks

- Generate demographic variables
- Generate baseline PASI
- Generate severity strata
- Generate prior biologic history
- Validate randomization balance

### Story 1.2.3: Simulate Longitudinal Outcomes

#### Tasks

- Generate repeated PASI measurements
- Model dose-response treatment effects
- Define true treatment effect parameters
- Store simulation truth values for future comparison

### Story 1.2.4: Simulate Intercurrent Events

#### Tasks

- Simulate rescue therapy
- Simulate treatment discontinuation
- Simulate adverse event withdrawals
- Simulate protocol deviations
- Simulate missing data under MAR assumptions
- Document all simulation assumptions

---

## Epic 1.3: Statistical Analysis Plan

### Story 1.3.1: Define Analysis Populations

#### Tasks

- Define Intent-to-Treat (ITT) population
- Define Safety population
- Define Per-Protocol population
- Define protocol deviation rules

### Story 1.3.2: Define Study Estimands

#### Tasks

- Develop ICH E9(R1) estimand framework
- Define treatment variable
- Define target population
- Define endpoint variable
- Define summary measure
- Define treatment policy strategy
- Define composite strategy

### Story 1.3.3: Define Intercurrent Event Handling

#### Tasks

- Specify rescue therapy strategy
- Specify treatment discontinuation strategy
- Specify missing data strategy
- Specify death handling strategy
- Document rationale

### Story 1.3.4: Define Multiplicity Strategy

#### Tasks

- Define primary endpoint hierarchy
- Define gatekeeping approach
- Define family-wise error control
- Document testing sequence

---

# Milestone 2: Primary Efficacy Analysis

## Epic 2.1: ANCOVA Primary Analysis

### Story 2.1.1: Prepare Analysis Dataset

#### Tasks

- Derive Week 16 change from baseline
- Create analysis-ready dataset
- Validate derived variables
- Perform QC checks

### Story 2.1.2: Fit Primary ANCOVA Model

#### Tasks

- Fit ANCOVA model
- Adjust for baseline PASI
- Adjust for severity stratum
- Adjust for prior biologic use
- Extract model estimates

### Story 2.1.3: Estimate Treatment Effects

#### Tasks

- Calculate LS means
- Calculate treatment contrasts
- Generate confidence intervals
- Generate p-values
- Compare estimates to simulation truth

---

## Epic 2.2: ANCOVA Diagnostics & Assumptions

### Story 2.2.1: Evaluate Model Assumptions

#### Tasks

- Create residual versus fitted plots
- Create QQ plots
- Create residual histograms
- Evaluate normality assumptions
- Evaluate linearity assumptions

### Story 2.2.2: Evaluate Variance Homogeneity

#### Tasks

- Perform Levene's test
- Assess homoscedasticity
- Document findings

### Story 2.2.3: Evaluate Alternative Methods

#### Tasks

- Compare ANCOVA versus t-test approaches
- Review non-parametric methods
- Review transformed endpoint approaches
- Review robust modeling approaches
- Document recommendations

---

# Milestone 3: Longitudinal Modeling & Missing Data

## Epic 3.1: MMRM Longitudinal Analysis

### Story 3.1.1: Create Longitudinal Dataset

#### Tasks

- Reshape dataset to long format
- Validate visit structure
- Validate subject-level records
- Verify missingness patterns

### Story 3.1.2: Fit MMRM

#### Tasks

- Specify fixed effects
- Specify visit effects
- Specify treatment-by-visit interactions
- Specify covariance structure
- Fit MMRM model

### Story 3.1.3: Estimate Longitudinal Treatment Effects

#### Tasks

- Estimate visit-specific treatment effects
- Estimate Week 16 contrasts
- Calculate confidence intervals
- Generate treatment profile plots
- Compare results with ANCOVA

---

## Epic 3.2: Multiple Imputation

### Story 3.2.1: Develop Imputation Strategy

#### Tasks

- Define imputation model
- Select predictor variables
- Define number of imputations
- Validate imputation assumptions

### Story 3.2.2: Execute Multiple Imputation

#### Tasks

- Generate multiple imputed datasets
- Fit analysis model within each dataset
- Pool estimates using Rubin's Rules
- Produce final inference

### Story 3.2.3: Assess Estimation Performance

#### Tasks

- Compare results with simulation truth
- Assess bias
- Assess coverage probability
- Assess precision

---

## Epic 3.3: Sensitivity Analysis

### Story 3.3.1: Implement Delta Adjustment

#### Tasks

- Define delta grid
- Apply adjustment scenarios
- Re-estimate treatment effects
- Record significance changes

### Story 3.3.2: Perform Tipping-Point Analysis

#### Tasks

- Identify tipping points
- Generate tipping-point heatmaps
- Evaluate robustness of conclusions
- Document findings

### Story 3.3.3: Assess MNAR Scenarios

#### Tasks

- Investigate departures from MAR
- Evaluate impact on efficacy conclusions
- Document regulatory implications

---

# Milestone 4: Secondary Endpoints & Multiplicity

## Epic 4.1: PASI75 Responder Analysis

### Story 4.1.1: Derive Binary Endpoint

#### Tasks

- Calculate PASI percentage improvement
- Derive PASI75 responder variable
- Validate endpoint calculations

### Story 4.1.2: Apply Endpoint Handling Rules

#### Tasks

- Implement non-responder imputation
- Handle rescue therapy subjects
- Handle discontinuations
- Handle missing observations

### Story 4.1.3: Analyze Binary Endpoint

#### Tasks

- Fit logistic regression model
- Estimate odds ratios
- Generate confidence intervals
- Conduct treatment comparisons

---

## Epic 4.2: Multiplicity Control

### Story 4.2.1: Execute Hierarchical Testing

#### Tasks

- Test primary endpoint
- Test High Dose versus Placebo PASI75
- Test Low Dose versus Placebo PASI75
- Document gatekeeping decisions

### Story 4.2.2: Evaluate Type-I Error Control

#### Tasks

- Review testing sequence
- Verify family-wise error control
- Document statistical conclusions

---

# Milestone 5: Negative Trial Scenario & Clinical Interpretation

## Epic 5.1: Negative Trial Simulation

### Story 5.1.1: Develop Alternative Scenario

#### Tasks

- Increase placebo response
- Decrease treatment effect size
- Increase variability
- Re-run simulations

### Story 5.1.2: Analyze Negative Trial Scenario

#### Tasks

- Repeat ANCOVA analysis
- Repeat MMRM analysis
- Repeat responder analysis
- Compare scenario outcomes

---

## Epic 5.2: Clinical Interpretation

### Story 5.2.1: Interpret Positive Results

#### Tasks

- Assess statistical significance
- Assess clinical relevance
- Evaluate benefit-risk considerations
- Summarize findings

### Story 5.2.2: Interpret Negative Results

#### Tasks

- Evaluate placebo response impact
- Evaluate power limitations
- Evaluate treatment effect magnitude
- Summarize findings

### Story 5.2.3: Draft Mock Clinical Discussion

#### Tasks

- Draft efficacy summary
- Draft limitations section
- Draft interpretation section
- Draft future recommendations

---

# Milestone 6: Reporting, Publication & Interview Showcase

## Epic 6.1: Final Reporting

### Story 6.1.1: Produce Publication-Quality Tables

#### Tasks

- Baseline characteristics table
- ANCOVA summary table
- MMRM summary table
- PASI75 summary table
- Sensitivity analysis table

### Story 6.1.2: Produce Publication-Quality Figures

#### Tasks

- Treatment profile plot
- Forest plot
- Residual diagnostics plots
- Missing data visualization
- Tipping-point heatmap

### Story 6.1.3: Render Final Report

#### Tasks

- Build Quarto report
- Generate HTML version
- Generate PDF version
- Validate reproducibility

---

## Epic 6.2: Portfolio Publication

### Story 6.2.1: Final Repository Polish

#### Tasks

- Refine README
- Add architecture diagrams
- Add workflow diagrams
- Review code quality
- Final repository cleanup

### Story 6.2.2: Interview Walkthrough Package

#### Tasks

- Create 5-minute project walkthrough
- Prepare estimand discussion
- Prepare ANCOVA discussion
- Prepare MMRM discussion
- Prepare missing data discussion
- Prepare sensitivity analysis discussion
- Prepare clinical interpretation discussion

---

# Definition of Done (DoD)

- All analyses are fully reproducible.
- All data are synthetically simulated.
- All code passes quality review.
- SAP and estimands are documented.
- ANCOVA and MMRM analyses are completed.
- Missing data analyses are completed.
- Sensitivity analyses are completed.
- Secondary endpoint analyses are completed.
- Final report is generated.
- GitHub repository is publication-ready.
- Project is interview-ready.

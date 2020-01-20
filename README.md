# `bel` MLOps
### The devil is in the details.

`bel` (will be) a modularizable library to deploy, log, monitor, and version informational products (data, ML, experiments) conforming to the general needs of MLOps, including

- Code version control
- Model version control
- ML system architecture & DAG
- Data versioning and monitoring
- Deployment
- Ongoing performance assessment
- Deployment distribution

Data science, ML, AI, and other frontier-level solutions are often seen as expensive in practice or out-of-reach for most budgets. However, the vast majority of the cost are due to repetitive, duplicative configuration and monitoring. General patterns exist, and `bel` is intended to support this.

---------------

### Notes from NIPS *Hidden Technical Debt in Machine Learning Systems*

#### Complex models erode the following boundaries:

- Entanglement: chaining together models adds fragility
- Correction cascades: correcting upstream models results in downstream entanglement
- Undeclared consumers: without knowing who uses the model, changes can result in expensive or dangerous couplings

#### Data dependencies are costlier than code dependencies

- Unstable data dependencies

- Underutilized data dependencies: including 
  - legacy features
  - bundled features
  - $\epsilon$-features
  - correlated features

- Static analysis of data dependencies

#### Feedback loops
- Direct loops
- Hidden loops

#### ML-system anti-patterns
- Glue code
- Pipeline jungles
- Dead experimental codepaths
- Abstraction debt
- Common smells: Plain-old-data type smell, multiple-language smell, prototype-smell

#### Configuration debt: specifying principles of good configuration
- It should be easy to specify a configuration as a small change from a previous configuration
- It should be hard to make manual errors, omissions, or oversights
- It should be easy to see, visually, the difference in configuration between two models
- It should be easy to automatically assert and verify basic facts about the configuration:number of features used, transitive closure of data dependencies, etc.
- It should be possible to detect unused or redundant settings
- Configurations should undergo a full code review and be checked into a repository

#### Dealing with changes in the external world
- Fixed thresholds of dynamic systems
- Monitoring and testing
  - Prediction bias
  - Action limits
  - Up-stream producers
  
#### Misc. areas of ML-related tech debt
- Data testing debt
- Reproducibility debt
- Process management debt
- Organization norms debt (mis-phrased as 'cultural' debt in the paper)

#### Measuring debt and paying it off: questions to assess
- How easily can an entirely new algorithmic approach be tested at full scale?
- What is the transitive closure of all data dependencies?
- How precisely can the impact of a new change to the system be measured?
- Does improving one model or signal degrade others?
- How quickly can new members of the team be brought up to speed?


---------------

### Sources

[0] https://papers.nips.cc/paper/5656-hidden-technical-debt-in-machine-learning-systems.pdf

[1] https://github.com/microsoft/MLOps

[2] https://slides.com/walsh/standards-in-ml-ops#/

[3] https://en.wikipedia.org/wiki/MLOps

[4] https://www.kdnuggets.com/2018/04/operational-machine-learning-successful-mlops.html

[5] http://www.machinelearning.ai/machine-learning/alejandro-saucedo-scalable-data-sciencemachine-learning-the-state-of-
dataops-mlops-in-2018/

[6] https://www.oreilly.com/radar/podcast/how-to-train-and-deploy-deep-learning-at-scale/

[7] https://searchdatamanagement.techtarget.com/feature/Machine-learning-algorithms-meet-data-governance

[8] https://petewarden.com/2018/03/19/the-machine-learning-reproducibility-crisis/

[9] https://conferences.oreilly.com/artificial-intelligence/ai-eu-2018/public/schedule/detail/68247

[10] https://bigdatabeard.com/bd-podcast-ep-34-putting-ai-to-work-with-mlops-powered-by-parallelm/

-------------

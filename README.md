# SAMfromSA_taf_template

TAF template for the SAMfromSA method: a SAM assessment on [stockassessment.org](https://stockassessment.org) brought into TAF.

The example is the Faroe Plateau cod assessment, `Cod_27_5b1` on stockassessment.org.

- `boot/sam_data.R` and `boot/sam_config.R`: download the data files and the model configuration of the assessment from stockassessment.org. The assessment is set by `sam_assessment` at the top of each.
- `data.R`: reads the data files and writes them as TAF tables, and sets up the SAM data.
- `model.R`: fits SAM with the configuration (`model_fit.R`), with retrospective and leave-one-out fits and residuals, and runs the forecast scenarios (`model_forecast.R`).
- `output.R`: the tables of the fit, Mohn's rho, and an FLStock object made with FLfse.
- `report.R`: the plots of stockassessment.org (`report_plots_saorg.R`), the plots and tables of the template (`report_plots.R`, `report_tables.R`), and the reports (`report_doc.R`): a Word and HTML report from `report.Rmd` and a quality report from `report_quality_report.qmd`.

Copied from [ices-taf-dev/wiki-example-stockassessment](https://github.com/ices-taf-dev/wiki-example-stockassessment) at commit 32e0b43.

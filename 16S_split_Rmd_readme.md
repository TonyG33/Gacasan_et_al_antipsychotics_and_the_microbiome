# Split R Markdown guide

This refactor separates the original notebook into two shareable documents.

## Files

- `16S_core_analysis.Rmd`: data import, phyloseq construction, alpha diversity, beta diversity, DESeq2 workflows, taxonomy summaries, relative abundance plots, and utility/export sections.
- `16S_metabolomics_integration.Rmd`: T6 pre-challenge subset, CLR genus processing, metabolomics preprocessing, Spearman association workflows, heatmaps, network plots, and DIABLO analyses.

## Notes

- The integration notebook is self-contained and rebuilds the `ps` object at the top.
- Duplicate chunk labels from the original file were renamed automatically to improve knitting and navigation.
- Iterative code was preserved rather than aggressively deduplicated so object dependencies would remain intact.

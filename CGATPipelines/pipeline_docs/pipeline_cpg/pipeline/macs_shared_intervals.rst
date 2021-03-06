======================
MACS Shared Intervals
======================

The following table presents the number of intervals in each dataset, 
which overlap with one or more intervals in all other datasets:

.. report:: macs_interval_comparison.SharedIntervals
   :render: table

   Intervals shared between all datasets

Length
------

The following plot shows the distribution of interval length for each set.

.. report:: macs_shared_intervals.sharedIntervalLengths
   :render: line-plot
   :transform: histogram
   :groupby: all
   :logscale: x
   :tf-aggregate: normalized-total
   :as-lines:

   Distribution of interval lengths

Average Coverage
----------------

The following plot shows the distribution of average interval coverage for each set.
The average coverage is the average number of reads covering the bins that constitute the interval.

.. report:: macs_shared_intervals.SharedIntervalAverageValues
   :render: line-plot
   :transform: histogram
   :groupby: all
   :tf-range: 0,50
   :tf-aggregate: normalized-total,reverse-cumulative
   :as-lines:

   Distribution of the average number of reads
   matching to bins within an interval.

Maximum Coverage
----------------

The following plot shows the maximum interval coverage for each set.
The maximum coverage is the maximum number of reads falling into the
bins that constitute an interval. The interval peak is the position with the maximum
number of reads.

.. report:: macs_shared_intervals.SharedIntervalPeakValues
   :render: line-plot
   :transform: histogram
   :groupby: all
   :tf-range: 0,100
   :tf-aggregate: normalized-total,reverse-cumulative
   :as-lines:

   Distribution of the number of reads at the peak within an interval.
   The distribution list the proportion of intervals of a certain peak
   value or more.

Fold Change
-----------

The following plot shows the fold change over control (input) for each set.

.. report:: macs_shared_intervals.SharedIntervalFoldChange
   :render: line-plot
   :transform: histogram
   :groupby: all
   :tf-range: 0,100
   :tf-aggregate: normalized-total,reverse-cumulative
   :as-lines:

   Distribution of fold enrichment for interval compared to control.

Closest TSS
-----------

The following plot shows the distance to the closest transcriptional start site for each set.

.. report:: macs_shared_intervals.SharedIntervalTSS
   :render: line-plot
   :transform: histogram
   :groupby: all
   :xrange: 0,100000
   :yrange: 0,1
   :tf-aggregate: normalized-total,cumulative
   :tf-range: 0,1000000,100
   :as-lines:

   Distribution of distance to the closest transcriptional start site

CpG Density
-----------

The following plot shows the distribution of CpG density for each set.

.. report:: macs_shared_intervals.SharedIntervalCpGDensity
   :render: line-plot
   :transform: histogram
   :groupby: all
   :as-lines:

   Distribution of CpG density


CpG Observed/Expected
----------------------

The following plots show the distribution of observed/expected CpGs for each dataset.
The expected number of CpG dinucleotides was calculated as the length of the sequence divided by the number of 
possible dinucleotides as in Takai and Jones PNAS (2002). 
The control dataset was generated by taking an interval of the same size 10kb upstream of the CpG island.

.. report:: macs_shared_intervals.SharedIntervalCpGObsExp1
   :render: line-plot
   :transform: histogram
   :groupby: all
   :as-lines:

   Distribution observed/expected CpGs (expected = length/16)


The following plots show the distribution of observed/expected CpGs for each set.
The expected number of CpG dinucleotides was calculated as the product of the number of C and G nucleotides 
in the interval divided by the interval length as in Emboss cpgplot.
The control dataset was generated by taking an interval of the same size 10kb upstream of the CpG island.


.. report:: macs_shared_intervals.SharedIntervalCpGObsExp2
   :render: line-plot
   :transform: histogram
   :groupby: all
   :as-lines:

   Distribution observed/expected CpGs (expected = nC*nG/length)


GC Content
-------------

The following plot shows the distribution of GC content for each set.

.. report:: macs_shared_intervals.SharedIntervalGCContent
   :render: line-plot
   :transform: histogram
   :groupby: all
   :as-lines:

   Distribution of GC content


---
title: "Milestone1-example"
author: "Matthew Connell"
date: "23/02/2020"
output: 
  html_document:
    keep_md: yes
    toc: true
---



## Autism Screening

### Data Description

The [dataset](https://archive.ics.uci.edu/ml/datasets/Autism+Screening+Adult)  used in this analysis was obtained from the University of California Irvine Machine learning Repository, uploaded by Fadi Thabtah. Each row represents an individual who participated in the survey. The survey's results, the app's classification, and some background information about the individual was recorded. Below is the entire variable set:

<table class="table table-condensed" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">  Variable              </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">  Type              </th>
   <th style="text-align:left;position: sticky; top:0; background-color: #FFFFFF;">  Description                                                                                                                             </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> A1_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: I often notice small sounds when others do not </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A2_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: I usually concentrate more on the whole picture, rather than the small details </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A3_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: I find it easy to do more than one thing at once </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A4_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: If there is an interruption, I can switch back to what I was doing very quickly </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A5_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: I find it easy to 'read between the lines' when someone is talking to me </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A6_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: I know how to tell if someone listening to me is getting bored </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A7_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: When I'm reading a story I find it difficult to work out the characters' intentions </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A8_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: I like to collect information about categories of things(e.g. types of car, types of bird, types of train, types of plant etc) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A9_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: I find it easy to work out what someone is thinking or feeling just by looking at their face </td>
  </tr>
  <tr>
   <td style="text-align:left;"> A10_score </td>
   <td style="text-align:left;"> Int (0,1) </td>
   <td style="text-align:left;"> Prompt: I find it difficult to work out people's intentions </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Age </td>
   <td style="text-align:left;"> Int </td>
   <td style="text-align:left;"> Age of the individual </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Gender </td>
   <td style="text-align:left;"> String </td>
   <td style="text-align:left;"> M (male) or F (female) </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Ethnicity </td>
   <td style="text-align:left;"> String </td>
   <td style="text-align:left;"> Common Ethnicities defined for each individual </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Born with Jaundice? </td>
   <td style="text-align:left;"> String (yes,no) </td>
   <td style="text-align:left;"> Was individual born with jaundice? </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Country of Residence </td>
   <td style="text-align:left;"> String </td>
   <td style="text-align:left;"> Home country of individual </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Used app before? </td>
   <td style="text-align:left;"> String (yes, no) </td>
   <td style="text-align:left;"> Has the user has used a screening app </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Result </td>
   <td style="text-align:left;"> Int </td>
   <td style="text-align:left;"> Cumulative score of the 10 survey Q's </td>
  </tr>
  <tr>
   <td style="text-align:left;"> age_desc </td>
   <td style="text-align:left;"> String </td>
   <td style="text-align:left;"> Age Group </td>
  </tr>
  <tr>
   <td style="text-align:left;"> relation </td>
   <td style="text-align:left;"> String </td>
   <td style="text-align:left;"> Parent, self, caregiver, medical staff, clinician ,etc. </td>
  </tr>
  <tr>
   <td style="text-align:left;"> ASD/Class </td>
   <td style="text-align:left;"> String (yes, no) </td>
   <td style="text-align:left;"> App's classification based on result </td>
  </tr>
  <tr>
   <td style="text-align:left;"> autism (Target Variable) </td>
   <td style="text-align:left;"> String (yes, no) </td>
   <td style="text-align:left;"> Does individual have an autism diagnosis? </td>
  </tr>
</tbody>
</table>

## Including Plots

You can also embed plots, for example:

![](milestone1-547-example_files/figure-html/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.

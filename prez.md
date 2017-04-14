---
title: LotikLabs
# theme: beige
# theme: black
# theme: blood
# theme: league
# theme: moon
# theme: night
# theme: serif
# theme: simple
# theme: sky
theme: solarized
# theme: white
# highlight-theme: github
highlightTheme: argate
separator: ----------------------------
verticalSeparator: v---------------------------
revealOptions:
    controls: true
    slideNumber: true
---

# Applied ML @ LotikLabs

Sayre Blades 

Note:
There will be some physics in this talk, so I hope you are ready.

----------------------------

## Who is Lotik?

http://samsungnext.com

http://lotik.com

Note:

(open samsung next link)

Lotik is partnerd with samsung next, a global investment initiative
within samsung.  Samsung next start is the division that targets
start ups. They provide lotik resources like: office space, HR, legal,
etc...

(talk about picture)

(back, open lotik link)

Lotik is a wireless water intelligence service.
- does anybody pay a water bill?
- why is usage monitoring important?


v---------------------------

## Who are you?

Data Engineer

- software engineer
- devops / architecture
- big data
- machine learning
<!-- .element: class="fragment" data-fragment-index="1" -->
  
Note:
Talk about my background

dont forget:
- machine learning

This is my first professional ML project.

v---------------------------

## Workflow

1. Data Collection <!-- .element: class="fragment grow highlight-current-blue" -->
1. Pre-processing
1. Analysis & Clensing
1. Modeling

Note:

(data science's less attractive sibling)

I am not a data science expert. Most of my career has mostly been
focused on data processing: moving data from one place to another;
storing it; retrieving it; building pipelines around it; and
productionizing it.

In data-science terms, its called pre-processing.

v---------------------------

### First Attempt

<img src="data-aq1.png" style="width: 40%;"/>

Note:

When I first joined the team, this is what data collection
looked like.  This is data to train/validate/test a
classification model.

no fun

Attempt to get ground truth.

v---------------------------

### Second Attempt

<img src="data-aq2-meter.png" style="float:left; width: 40%;"/>
<img src="data-aq2-bath.jpg" style="width: 40%;"/>
<img src="data-aq2-toilet.jpg" style="width: 40%;"/>

v---------------------------

### Third Attempt

<img src="data-aq3.png" style="width: 40%;"/>

----------------------------

## Workflow

1. Data Collection
1. Pre-processing <!-- .element: class="fragment grow highlight-current-blue" -->
1. Analysis & Clensing
1. Modeling

Note:

Here I will talk about taking the data in its raw form and
converting it to a format that is consumable by our models.

v---------------------------

## Raw format

metadata file

				pipe type: braided
				pipe size: 3/8
				fixture: bath sink auto
	Started collection at: 2017-04-10 14:15:40.098894
			stopped at: 2017-04-10 22:06:31.078903
	Total number of rows: 11,541,037
				rows/sec: 408.518111453950

csv data file

	x,y,z,pulses
	-0.8862,0.0303,0.2824,0
	-0.9487,0.0254,0.2882,0
	-0.9555,0.0283,0.3009,0
	-0.9546,0.0244,0.2970,0
	-0.9565,0.0264,0.2941,0
	-0.9555,0.0254,0.3009,0
	-0.9575,0.0274,0.2970,0
	-0.9536,0.0274,0.2931,0
	-0.9516,0.0274,0.3000,1

v---------------------------

## Gen 2 format

	time     rms_x   rms_y   rms_z    corr    zcr      flow  label
	18:15:49 0.00716 0.00297 0.00522  0.01446 60.00000 0.000 Off
	18:15:50 0.00331 0.00322 0.00552  0.01086 69.33333 0.000 Off
	18:15:51 0.00305 0.00306 0.00578  0.02608 66.00000 0.000 Off
	18:15:52 0.00300 0.00303 0.00584 -0.04534 59.00000 0.000 Off
	18:15:53 0.00334 0.00308 0.00582 -0.05407 54.33333 0.000 Off
	18:15:54 0.00286 0.00302 0.00613 -0.07043 66.33333 0.000 Off
	18:15:55 0.00290 0.00300 0.00584  0.03176 60.00000 0.000 Off
	18:15:56 0.00377 0.00421 0.00650  0.09796 47.00000 0.000 Off

v---------------------------

## Gen 3 format

	time               x        y       z      p  ml_bf
	18:15:49.065448999 -0.9399  0.1182  0.3410 0  0.158730
	18:15:49.067896000 -0.9380  0.0840  0.3234 0  0.158730
	18:15:49.070344000 -0.9340  0.0410  0.3097 0  0.158730
	18:15:49.072792000 -0.9663  0.0449  0.2032 0  0.158730
	18:15:49.075240000 -0.9800  0.0274  0.2267 0  0.158730
	18:15:49.077688000 -0.9360  0.0420  0.2228 0  0.158730
	18:15:49.080136000 -0.9106  0.0117  0.2081 0  0.158730
	18:15:49.082584000 -0.9419 -0.0234  0.2237 1  0.158730

----------------------------

## Workflow

1. Data Collection
1. Pre-processing
1. Analysis & Clensing <!-- .element: class="fragment grow highlight-current-blue" -->
1. Modeling

v---------------------------

<img src="rms-analysis.png" />

v---------------------------

<img src="gen3-rms.png" style="float:left; width: 45%;"/>

<img src="gen3-spec.png" style="float:right; width: 45%;"/>

----------------------------

## Workflow

1. Data Collection
1. Pre-processing
1. Analysis & Clensing
1. Modeling <!-- .element: class="fragment grow highlight-current-blue" -->

v---------------------------

## Palladium

https://pypi.python.org/pypi/palladium/

----------------------------

## Thanks

    email: sblades@samsungnext.com
    github: SayreBlades

Note:
If you would like access to these slides feel free
to drop me a line.

# Lecture 2 Non-Personalized Recommendation Systems #


## Services: ##

* [Zagat](http://www.zagat.com/)  - Restaurant, average * 10 on a 4-scales
	* 
* [CN_Travel](http://www.cntraveler.com/) - Tour, percentage of people
* [Billboard](http://www.billboard.com/) 

All of them are *Non-Personalized*

---
Averages can be misleading:

* Lack context
* Lead to the concept of product association recommendations

So, *People who X also Y* is important, but how? Three possible solutions

* User profiles
* Transaction data
* Time-window on user profiles

, and their equations might be
$$ \frac{P (X \cap Y) } {P(X)}$$

---

### Challenge : It did not compensate the popularity of Y ###

S2 : Does X make Y more likely?

$$ \frac{ \frac{X \cap Y}{X}}{\frac{\neg X \cap Y}{\neg x}} $$
In data mining, association rule mining brings the *lift* metric.
\\[ \frac{(  P(X \cap Y)}{P(X) * P(Y)} \\]

* People who don't like them, don't go. So the scores have bias *Self-selection bias*. 
*  *Increased diversity of raters* - makes rating go toward average. 

---
1. Non-personalzed averages can be effective in **Right applications**
2. Product associations can provide useful recommendations in a **context**.
3. Still face challenges in a **Diverse Population** in a cluster. 

##Think  How to Program? 
---
##2-2 Preferences and Ratings##

We need data. 

Data comes from users. So we need to know what,  and how, to collect data.

---

##Star Ratings

* Widely-used interface
* Several design decisions
* 5, with or without 1/2, is very common.
* Example: Netflix, Goodreads, Amazon, MovieLens
* Provide calibration

## Thumbs and Likes ##

* Vote up/down
* Ephemeral items that don't have long-time stands.
* Very low cost to rate.
* Example: Youtube, News (reddit, Digg), Q&A like 

Other interfaces:

* Continuous scales
* Hybrid ( 1-100 + never again)
* Temporary (30-day suspends from Pandora)

When are rating provided?

* At Consumption
* Memory
* Expectation -  the user has not been experienced

### Difficulties With Rating ###

* Noise in the rating, e.g., shift in rating from a same user.

---
## Implicit Data ##

Collected from users actions. It is usually for other purposes and not expressing preference. Usually, their action say a lot.

1. **Reading Time** - early implicit data, in video and music applications.
2. **Binary Actions** - Click, don't click, purchase, Follow/Friend.


---
## Lecture 2.4 Scales and Normalization ##


### Ranking Considerations ###

* Confidence
* Risk tolerance
* Domain and business considerations
---

**Damped Means**
$$ \frac{\sum_u r_{ui} + k\mu}{n+k}$$ 

**Confidence Intervals**

* Lower bound: conservative
* Upper bound: might be amazing

**Domain Consideration : Time **

The *Reddit* uses
\\[\frac{(U-D-1)^\alpha}{(t_{now} - t_{post})^\gamma} * P \\]
$$\alpha$$, where the decay parameter, is 0.8
$$\gamma$$, Gravitiy, 1.8
P is the penalty, determined by company as to marketing strategies.  -- Service-dependent

Check The *Reddit* rules:

\\[ \log_{10}\\]

The ranking could be manipulated for 'good' or 'evil'. Most important case also easiest to hand-modify. 

---
##2.5 Preferences and Rating - Interview with Anthony Jameson

Three and one new patterns from users:

* Attribute-Based : attributes in customers mind
* Consequence-Based : what people get or happen
* Experience-Based : case-based or content-based. What is done in the past. 
* Another: Socially-Based

Irrational? 

	Help people to make a choice. Sometimes the system just support 
	users in occasional cases instead of taking the whole phase. There 
	are actually several patterns. What will happen if I buy this 
	dictionary, which is consequence-based. In fact, in many cases the 
	feeling you have when looking at things are reflections of the
	experience you have had in the past, and could be quite reliable
	guide.  
		The next pattern we have here is socially pattern. What
	recommenders already do is the calloborative filtering. What 
	recommenders could do is to recommend with regard to a reference 
	group. This is even less normatively optimal than just basing your 
	choice on own experience. In many cases, the best information 
	available is what other people known. 
	
* People 'like you choose' - Collaborative filtering
* Social influence, they want to identify with a different group.
* Simply to conform with other people on a practical level, to share thing.

Trusted recommendations are recommendations from people they know, rather than people have actually have better taste. Collect info from users past experience. Some patterns of behavior is easier to mis-interpret if you don't understand how they come about through choosing processes. The switching cost is high to people sometimes. The whole notion of having general liking or preferences in not as solid as one thinks. Expect student to think about more fundamentally in what the recommendations really is and what the underlying logic is. 










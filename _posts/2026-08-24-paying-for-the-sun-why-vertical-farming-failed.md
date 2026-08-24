---
layout: post
title: "Paying for the Sun: Why Vertical Farming Failed"
date: 2026-08-24 09:00:00 -0700
category: economics
categories: [economics]
tags: [agriculture, energy, thermodynamics, venture-capital, agtech, food-systems]
subtitle: "How an Industry Raised $5 Billion to Buy Sunlight"
description: >-
  Vertical farming raised billions on the promise of growing food indoors at
  scale. It collapsed because of physics: LEDs convert roughly 2% of input
  electricity into plant biomass, the other 98% becomes heat you have to pay
  to remove, and no crop denser than lettuce can survive that math.
seo:
  type: BlogPosting
---

In 2021, a company called Bowery Farming was worth $2.3 billion. It grew
lettuce. Not a lettuce futures exchange, not a lettuce logistics platform —
lettuce, in a warehouse, in New Jersey. Three years later it was worth
nothing, and the warehouses were dark.

This is the story of an industry that raised something like five billion
dollars to solve a problem that turned out to be a law of physics.

<!--more-->

---

## 1. The Silicon Valley Mirage

The pitch was, genuinely, one of the best pitches of the 2010s.

Here it is: agriculture uses about half the habitable land on Earth and
roughly 70% of global freshwater withdrawals. It is dependent on weather,
which is becoming less predictable. Its output travels an average of well
over a thousand miles to reach an American plate, losing freshness and
nutrition the entire way. And it is the last major industry that has not been
brought indoors, instrumented, and optimized.

So: bring it indoors. Stack the growing beds vertically to multiply yield per
square foot. Replace the sun with LEDs, which had just gotten dramatically
cheaper. Recirculate the water, cutting usage by 95%. Eliminate pesticides
because there are no pests in a sealed room. Put the farm inside the city, so
the lettuce travels ten miles instead of two thousand. Then run the whole
thing on sensors and machine learning, and improve it every season the way
software improves — compounding, not linear.

It is a *beautiful* pitch. It has a technology story, a climate story, a
supply-chain story, and a health story, and every one of them is real. That
is why the money came.

AeroFarms, founded 2004, built a flagship facility in Newark, New Jersey and
raised in the neighborhood of $200 million. Plenty, founded in South San
Francisco in 2014, pulled in over $900 million — including a $200 million
round led by SoftBank's Vision Fund in 2017, with money from Jeff Bezos and
later a strategic investment and supply deal from Walmart. Bowery Farming,
founded 2015, raised roughly $700 million from GV, GGV, Temasek and others,
peaking at that $2.3 billion valuation in a 2021 round. Add Infarm in Berlin,
Fifth Season in Pittsburgh, Kalera in Orlando, Upward Farms in Brooklyn, and
dozens more, and you get an industry that absorbed somewhere between four and
five billion dollars of private capital in seven years.

And here is where the story turns, and the turn is almost too neat.

The pitch was written in an era of essentially free money and cheap,
stable energy. Both of those conditions ended in the same eighteen months.

Interest rates went from near zero to over five percent between March 2022
and mid-2023, which meant capital-intensive businesses with long payback
periods were suddenly being discounted at a completely different rate.
Simultaneously, the 2022 energy shock sent industrial electricity prices up
sharply across Europe and meaningfully across the US. For a normal software
company, the first shock hurts. For a company whose product is *literally
converted electricity*, both shocks hit the same line item.

The bankruptcies came in a wave.

Fifth Season shut down abruptly in October 2022. Infarm — which had been
operating in-store growing units across European supermarkets — announced a
retreat from most of Europe in late 2022 and cut the majority of its staff.
AppHarvest, the Kentucky greenhouse company that had gone public via SPAC at
a billion-dollar valuation, filed for Chapter 11 in July 2023. Kalera filed
in 2023. AeroFarms — the standard-bearer, the one with the TED talk — filed
Chapter 11 in June 2023, emerged as a smaller company built around a single
Danville, Virginia facility, and stopped being the future of food. Bowery
Farming, after quietly closing facilities and shedding staff through 2024,
ceased operations entirely in November 2024. And in March 2025, Plenty — the
best-funded of all of them — filed for Chapter 11, closed its Compton,
California leafy greens facility, and pivoted what remained toward
strawberries in Virginia.

The industry's own explanation was that this was a funding winter. Cheap
capital dried up, growth-stage companies that hadn't reached profitability
died, and that's a story you could tell about a hundred sectors in 2023.

But that explanation has a problem: the funding winter is what *killed* them.
It is not what made them unprofitable. They were unprofitable the entire
time, and they were unprofitable for a reason that no amount of scale,
software, or patience was going to fix.

---

## 2. The Thermodynamics Trap

Start with a number that sounds like it should be good news: LEDs are
efficient.

They are. A modern horticultural LED fixture converts a genuinely impressive
share of the electricity you put into it — around 40% at the system level,
once you account for driver losses, thermal derating, and the fact that
you're running a whole rack, not a single diode on a lab bench — into
photosynthetically active radiation. The best red diodes, measured in
isolation, do better. But 40% wall-plug-to-usable-photons is a fair number
for a real farm.

Then you lose some more. Not every photon that leaves the fixture lands on a
leaf. Some hits the tray, the wall, the gap between plants. Call canopy
interception and absorption 85%, which is generous — it assumes a well-tuned
system with a closed canopy.

And then you hit the part that no engineer gets to optimize.

Photosynthesis is not efficient. The theoretical ceiling for a C3 plant —
wheat, rice, lettuce, soy, most of what we eat — is around 4.6% of absorbed
light energy converted into chemical energy in biomass. In a field, real
crops manage around 1%. Indoors, with CO2 enrichment, perfect water,
perfect nutrients, and light tuned to the exact wavelengths chlorophyll wants,
you can push toward the ceiling. Call it 4.5%. That is the best-case number.

Now multiply the chain:

> **0.40** (wall plug → PAR) **× 0.85** (delivered and absorbed) **× 0.045**
> (photosynthetic conversion) **≈ 1.5%**

Round it up, be charitable, call it **2%**.

Two percent. For every hundred joules of electricity you buy, two joules end
up as plant.

And now the part that turns a bad number into a fatal one.

Where do the other ninety-eight joules go?

They become heat. All of them. This is not a metaphor or an approximation —
it is conservation of energy in a sealed box. Every watt that enters that
grow room and does not leave as chemical energy in a lettuce leaf leaves as
thermal energy in the air. The inefficiency of the LED becomes heat at the
fixture. The photons that miss the leaf become heat at the surface they hit.
The photons that hit the leaf and aren't converted become heat in the leaf.
There is no third destination.

So a vertical farm running one megawatt of lighting is, from an HVAC
engineer's point of view, a one-megawatt space heater with a plant collection.

And you cannot open a window. The entire value proposition — no pests, no
pathogens, controlled humidity, controlled CO2 — depends on the room being
sealed. So you have to actively pump the heat out. Chillers do this at a
coefficient of performance of roughly 3 to 4, meaning it costs you about a
quarter to a third of a watt to move a watt of heat.

That's a 25–35% surcharge on the lighting bill. Every hour. Forever.

And it gets worse, because heat is only half the load. Plants transpire.
A leafy-green farm can move on the order of a couple of liters of water into
the air per square meter of canopy per day, and all of that has to be
condensed back out — and the latent heat of vaporizing water is enormous
compared to the sensible heat of warming air. On many indoor farms,
dehumidification is a larger HVAC load than cooling. You are paying to
evaporate the water and then paying again to condense it, and the "95% water
savings" headline is what you get *after* you've spent the electricity to
recapture it.

Add fans, pumps, controls, and the fact that all of this runs 8,760 hours a
year with no seasonal relief, and the operating cost structure of a vertical
farm looks like this: energy is not a line item. Energy is the business, with
some plants attached.

Which raises the obvious question. Sunlight delivers roughly a kilowatt per
square meter, for free, to every field on Earth, and has done so reliably for
four billion years. What exactly is the argument for buying it?

---

## 3. The Biological Wall

The industry's answer — and for a while it was a genuinely good answer — was:
*we're not selling calories, we're selling produce.*

And that's the trick that made lettuce work.

Lettuce is about 95% water. A kilogram of it contains roughly 150 kilocalories
of food energy. That is almost nothing — a kilogram of lettuce has less usable
energy than two tablespoons of olive oil. When you buy lettuce, you are not
buying nutrition in any meaningful caloric sense. You are buying crunch,
freshness, volume, and the absence of slime.

That is exactly the right product for an indoor farm, because it means the
photosynthesis you have to pay for is minimal. A leafy-green facility runs
somewhere in the range of 8 to 15 kilowatt-hours of electricity per kilogram
of product, all-in. Take a 500-gram head at 10 kWh/kg: about 5 kWh, or
somewhere around 25 to 60 cents of electricity at industrial rates. Against a
retail price of several dollars, that is survivable. Not comfortable —
survivable.

It is also, in energy terms, completely insane. You have spent roughly 8,600
kilocalories of electricity to produce 150 kilocalories of food. That is a
57-to-1 energy loss, and it only escapes notice because nobody eats lettuce
for energy.

Now try to feed someone.

Take a loaf of bread. A standard 800-gram loaf uses about 570 grams of flour,
which at ~75% milling extraction requires about 750 grams of wheat grain.
That grain contains roughly 2,550 kilocalories, or about 2.97 kWh of chemical
energy.

But you can't grow only the grain. Wheat's harvest index — the fraction of
above-ground biomass that ends up as edible kernel — is about 0.45 in modern
varieties. So the plant has to build about 6.6 kWh of total biomass to hand
you 2.97 kWh of grain.

Run that backward through the efficiency chain from Section 2:

- Biomass energy required: **6.6 kWh**
- At 4.5% photosynthetic conversion → light energy delivered to canopy:
  **~147 kWh**
- At 85% interception and 40% fixture efficiency → lighting electricity:
  **~430 kWh**
- Add ~30% for HVAC, dehumidification, fans and pumps: **~560 kWh**

**Five hundred and sixty kilowatt-hours of electricity. For one loaf of
bread.**

At a favorable US industrial power rate of $0.06–$0.09 per kWh, that is
roughly **$30 to $50 of pure electricity per loaf** — and that is the raw
energy alone. It does not include the building, the racks, the lights
themselves, the HVAC hardware, the labor, the seed, the nutrients, the
milling, the baking, or any return on the capital that built the place.

For comparison: 560 kWh is roughly what a typical American household consumes
in three weeks. It is enough to drive an electric car about 1,800 miles. You
would be spending it on a loaf of bread that costs $3.49 at the store, grown
by a farmer in Kansas whose primary energy input arrived for free.

And this is not a number that engineering fixes. Look at where the loss
actually lives. The fixture efficiency could plausibly improve from 40% to
60% — that's a real, achievable target, and it takes the loaf from 560 kWh
to about 390 kWh. Meaningful. Not remotely enough. The dominant term in that
chain is the 4.5% photosynthetic conversion, and that number is not an
engineering parameter. It is set by the quantum mechanics of chlorophyll
and the biochemistry of RuBisCO, an enzyme so inefficient that it routinely
grabs oxygen instead of carbon dioxide and has been under selection pressure
for three billion years without getting appreciably better.

You cannot Moore's Law your way past a photon budget.

So the biological wall is this: indoor farming is viable in inverse proportion
to how much food value the crop actually contains. The higher the calorie
density, the worse the math. Lettuce, herbs, microgreens, and strawberries sit
on the viable side. Wheat, rice, maize, soy, potatoes — the crops that supply
roughly two-thirds of human caloric intake — sit so far on the other side that
the gap is not a matter of percentages: about 10 kWh per kilogram of
lettuce against roughly 750 kWh per kilogram of wheat grain — very nearly
two orders of magnitude.

Vertical farming was never going to feed cities. It was always going to
garnish them.

---

## 4. The Grocery Store Reality Check

Which would be fine, except for one more problem: garnish is a commodity.

Here is the retail scene as it actually played out, roughly 2022 through 2024.
In the refrigerated case, a 4- to 5-ounce clamshell of indoor-grown baby
greens: pesticide-free, triple-washed or wash-free, grown ten miles away,
beautifully packaged, priced around **$4.99**. Two feet away, a head of
romaine trucked in from Yuma, Arizona: **$1.49**.

Vertical farming's founders were not naive about this. The bet was that the
gap would close from both directions — that indoor costs would fall with
scale and automation, while field costs would rise with drought, labor
shortages, water restrictions, and recall risk. There was real evidence for
the second half. California and Arizona water allocations were tightening.
E. coli recalls in romaine were a recurring national story. Labor was scarce.

But the gap didn't close, for three reasons that compound.

**First, the field competition is extraordinarily good at this.** Yuma,
Arizona supplies something like 90% of US leafy greens in winter; the Salinas
Valley covers summer. That system has had a century to optimize. The land is
already paid for. The primary energy input is free. Harvest is mechanized to
a degree most people don't appreciate — rigs that cut, wash, and pack in the
field at walking speed. The cold chain from Yuma to a Chicago distribution
center is a solved logistics problem measured in dollars per pallet. Against
that, "we saved on freight" is a rounding error, and it comes bundled with a
warehouse in an urban industrial zone where rent is ten to a hundred times
farmland.

**Second, the capital cost never amortized away.** Building indoor growing
capacity runs on the order of $100 to $200+ per square foot of growing area —
racking, LEDs, HVAC, fertigation, controls, automation. That is a
manufacturing plant, not a farm. Depreciation and interest on it show up in
every clamshell whether the facility runs at 40% utilization or 95%. And
because each new facility is a fresh capital outlay, growth *consumes* cash
rather than generating it. Software scales because the second copy is free.
A second vertical farm costs exactly what the first one did, plus inflation.
The industry sold a software growth story on a heavy-industry cost structure,
and the two only look alike on a slide.

**Third — and this is the one that actually broke the timing — the consumer
went the wrong way.** US grocery inflation ran near double digits in 2022,
the sharpest in four decades. The measured consumer response was not to
reward premium provenance. It was to trade down: private label share climbed,
club-store and discounter traffic climbed, unit sizes shrank. A $4.99
clamshell whose entire value proposition is *virtue and freshness* is
precisely the SKU that gets abandoned when a shopper's basket total is up
fifteen percent year over year.

So the industry ran the standard playbook and it failed in the standard way.
Cut price to win shelf space, and you erase a margin that was already thin.
Hold price, and volume stalls, which strands the fixed costs that were
supposed to be diluted by volume. Bowery and Plenty both ended up here:
significant retail placement, real product quality, genuine customer
affection — and single-digit percentage share of a category where the
incumbent's marginal cost was a fraction of theirs. You do not out-scale a
competitor whose energy bill is zero.

---

## What Actually Survived

The instructive part is what didn't die.

**Greenhouses.** The Dutch model — glass, sunlight, supplemental LEDs only
when the daily light integral falls short — is a real, profitable,
century-old industry. It uses roughly an order of magnitude less purchased
energy per kilogram than a sealed vertical farm for the simple reason that it
takes the free photons first and buys only the shortfall. Tomatoes,
cucumbers, and peppers in North American supermarkets are already
substantially greenhouse-grown, and nobody calls it disruption.

**High-value-per-kilogram crops.** Strawberries, culinary herbs, wasabi,
cannabis, seedlings and transplants, and plant-made pharmaceutical compounds.
The common thread: the crop sells for enough per kilogram that a
several-dollar energy input disappears into the margin. Plenty's post-
bankruptcy pivot to strawberries is not a retreat into a niche. It is the
correct read of the physics, arrived at expensively.

**The technology itself.** LED spectrum tuning, fertigation control, climate
sensing, and crop-vision systems developed for vertical farms are being
absorbed into greenhouses and controlled-environment horticulture, where they
work fine. The R&D wasn't wasted. The business model around it was.

---

## The Transferable Lesson

The failure mode here is more general than agriculture, and it is worth
naming precisely, because it will happen again.

Vertical farming's core proposition was to replace a free, abundant,
infinitely renewable input — sunlight — with a purchased one. Every other
claimed advantage was real: less water, less land, no pesticides, shorter
freight, year-round supply, no weather risk. All true. All genuinely valuable.
And all of it had to be paid for out of a margin that started at a 98% energy
loss and then got charged a second time to remove the waste heat.

There is a category of business where scale fixes the unit economics — where
the marginal cost curve bends down and the whole model comes good at volume.
That category is defined by fixed costs dominating variable ones. Vertical
farming was the opposite: its dominant cost was variable, physical, and
indexed to the price of electricity, which meant every additional kilogram of
lettuce cost approximately what the last one did. Growth didn't fix it.
Growth *scaled* it.

Five billion dollars discovered that the sun is not a market inefficiency.
It's just free.

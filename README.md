GovHack 2013 - Team Trample
=======

## Background

I signed up to GovHack 2013 on a whim, and arrived on the first night not knowing anybody there.  I ended up forming a
team with 5 others (mostly non-developers) who I met on the night and we proceeded to hack away trying to do something interesting with
public transport data for Melbourne.

Our software development practicies left something to be desired.  Actually, we didn't really develop software - just
hosted a PostgreSQL/PostGIS database, populated it with data and displayed it using TileMill.

Anyway, it was a requirement that we publish some sort of code on GitHub.  This repository contains all the relevant
code we could find.

## The Project

We decided to make a heat map of public transport access in Melbourne.  

None of us had any kind of experience with GIS before, so we spent most of our time trying to understand the 
different tools and data formats and how to put it together into something that vaguely did what we want.

We ended up looking at every mesh block within a certain distance of Melbourne, and for each mesh block we calculated
the number of train stations, tram stops and bus stops nearby.  

Those numbers fed into a formula that calculated a 'heat' value for the mesh blocks.

The mesh blocks and related 'heat' values were pulled into TileMill, and coloured using TileMill styling rules.

## Outcome

We ended up having a basic map that did correctly show different heat values across mesh blocks.

The
final map was still missing key features (e.g. a legend, overlaying major roads and suburb boundaries) and ended up
delivering much less than our original ambitions (we'd originally intended to highlight areas with high population density
but low transport access as a priority for transport planning...).

The TileMill server was hosted on an AWS instance for a few weeks after GovHack, but I ultimately stopped it so that 
I could run other projects.  We never ended up rendering it into a finished presentation-quality image so unfortunately
there isn't a record of our work out there.

On the plus side, we did win the 'Spirt of Govhack' award for Melbourne partly in recognition of the fact that we were
one of the few teams that met on the night and didn't know each other beforehand.

Some more informtion about the team and a video can be found on the
[GovHack Hackerspace](http://hackerspace.govhack.org/?q=groups/transprox).

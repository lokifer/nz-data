#NZ data

Although statistical data about the census, elections etc. is freely available on Government websites, it requires a considerable amount to effort to find, collate and put into a useful form.

Political parties campaigning, media outlets and analysts etc. have the resources to do this - for everyone else it's time-consuming and tedious.

We'd like to try to remove this barrier to entry so that everyone can make use of it; to better make informed decisions, or to create infographics, web apps and anything else it might be useful for.

Initially we're focussing on just the election results from the MMP general elections held to date.

To start with:

- Election results
- Election polling
- Census data

We're just going to pick away at it when we have time, so contributions would be extremely welcome, either of normalised data in a useful format such as json, xml or csv, or pointers to usable data on the web.  

You can help by either getting in touch with me via [email](mailto:nrkn.com@gmail.com) or sending me a pull request on Github.

##Resources & Data Sources

- [Wikipedia](http://en.wikipedia.org)
- [Stats NZ](http://www.stats.govt.nz/)
- [data.govt.nz](https://data.govt.nz/)
- [ict.govt.nz](http://ict.govt.nz/)
- [Dept of Internal Affairs data](http://www.dia.govt.nz/Data-and-statistics)
- [Open NZ](https://wiki.open.org.nz/wiki/display/main/Welcome)
- [University of Auckland database links to New Zealand statistical data](https://www.library.auckland.ac.nz/databases/record/?record=NZStats)

##It would be really nice to get pull requests with:

- Candidate and electorate seat data for each year
- Census data (ie. how many people were 18+ and therefore eligible but didn't enrol)
- Opinion poll results

The next thing we'll be doing is adding the detailed voting data, from:

http://www.electionresults.govt.nz/electionresults_1996/pollingplaces.html

Sadly these are all PDFs containing images scanned from paper, they'll need to be OCR'ed and verified :/

Perhaps they are available elsewhere?

##Example:

```javascript
{
  "1996": {
    "date": "12/10/1996",
    "parliamentNumber": 45,
    "wikiSlug": "New_Zealand_general_election,_1996",
    "registered": 2418587,
    "results": {
      "National": {
        "partyVote": 701315,
        "electorateSeats": 30,
        "listSeats": 14
      },
      "Labour": {
        "partyVote": 584159,
        "electorateSeats": 26,
        "listSeats": 11
      },
      ...
    },
    "informal": 8183,
    "disallowedSpecial": 54633
  }
}
```

##Possible uses

###NZ data visualisation thing

I think it would be interesting to make an open source web app for visualising NZ statistical data, particularly election and polling data.

Probably with [d3](http://d3js.org/)

Any ideas, contributions, corrections etc. welcomed.

####Plan

A visualisation of a horizontally panning timeline divided into months, starting with the first MMP election in 1996:

1. If it was the month the election was held in, the result of the general election in a data box with various stats.
2. If not, poll data for that month where available, otherwise interpolated between the last available poll or election result and the next available.

![](timeline.png)


##License

As far as I understand it all of the data is already in the public domain. 

The software (tool, utilities etc.) are licensed under: 

The MIT License (MIT)

Copyright (c) 2014 Nik Coughlin

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

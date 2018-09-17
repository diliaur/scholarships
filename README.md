# Display Sheets

## Basic About

This is a small app to allow filtration and search of [CSEAS](http://www.cseashawaii.org) compiled (mainly Southeast Asia-focused) scholarships and fellowships (a re-do of the site's [scholarships page](http://www.cseashawaii.org/students/scholarships/)). It pulls in data from a Google Sheet of the scholarships, allowing for easy editing without touching code, and presents it in sortable/filterable form. See _Libraries Explored or Used_ for which JS libraries enable this.

## To Do

- [ ] Add description to page & terminology key as in old/index.html
- [ ] To save space, make the description & key toggle-able
- [ ] Sticky first column (award names) (maybe)
- [ ] Make header row (and maybe search bar also) sticky
- [ ] Add responsive sidebar to house checkbox filtration or other info
- [ ] Add checkbox filters (on certain columns only)
- [ ] Find a more robust way to pull this off.
	- _2018/09/05_ Need the simplicity of Google Sheets for non-technical users to edit the spreadsheet & don't want to build a whole other (ungeneralizable) mini-CMS just to plug back into wordpress. But also don't want to risk the whole project going offline if the API breaks. Maybe can use Tabletop to export the spreadsheet & cache that.

## Done
- [x] (2018-09-10) Add filtration system on scholarship award metadata
	- integrated Tabletop with Listjs to generate a table rather than writing custom templating. Fixes issue `2018/09/05` below. Filtering and sorting now work. This is currently being constructed in scratch.html/js/css (files to be consolidated later)

## Issues & Notes

- **RESOLVED** _2018/09/05_ Tried List.js with the JS-generated list of scholarship awards and it broke the page (lol). Could be because the awards are inserted into the DOM via JS & List.js refreshes the DOM somehow, but the scholarship list generator isn't called again. There's a way to construct a list in List.js so maybe this is the way to go, rather than the custom template currently used.

## Libraries explored or used

- [Tabletop.js](https://github.com/jsoma/tabletop) - read in google sheet data
- [List JS](listjs.com) - filtration, sorting, and template output
- [jQuery](https://jquery.com/)

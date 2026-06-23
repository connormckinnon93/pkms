---
tags:
  - type/structure
  - structure/list
  - chart/bar-chart
  - theme/zettelkasten
  - type/dataviewjs
  - target/starterkit
aliases:
created: 2026-06-22, 17:15
modified: 2026-06-22, 17:15
template_type: Structure
cc: CC BY-SA 4.0
source: https://github.com/groepl/Obsidian-Templates
view_count: 1
---

# 7 Days - Modified

| [7 Days - Created](7%20Days%20Created%20Chart.md) | [7 Days - Summary](7%20Days%20Created%20List.md) | [7 Days - Modified](7%20Days%20Modified%20Chart.md) | [7 Days - Table](7%20Days%20Table.md) |

<!-- Main STRUCTURE of my content -->

```dataviewjs 

// === 7 Days Chart ===

// --- Age ---
var first_note = "20260622";
var a = moment();
var b = moment(first_note);
var age_years = a.diff(b, 'years');
var age_weeks = a.diff(b, 'weeks');

// --- Last 7 Days ---
var a = moment().format("YYYY-MM-DD");

var b = moment().subtract(1, 'week');
b = moment(b).format("YYYY-MM-DD");

var c = moment().subtract(1, 'month');
c = moment(c).format("YYYY-MM-DD");

var d = moment().subtract(3, 'month');
d = moment(d).format("YYYY-MM-DD");

var e = moment().subtract(6, 'month');
e = moment(e).format("YYYY-MM-DD");

var f = moment().subtract(1, 'year');
f = moment(f).format("YYYY-MM-DD");

var g = moment().subtract(2, 'year');
g = moment(g).format("YYYY-MM-DD");

// —— Last 1 Week —-
var count_note_1w = dv.pages('"3_Permanent"').where(p => p.modified >= b).length;

// —— Last 1 Month —-
var count_note_1m = dv.pages('"3_Permanent"').where(p => p.modified >= c).length;
var count_note_1m_13 = (count_note_1m / 52 * 12).toFixed(1);

// —— Last 3 Month —-
var count_note_3m = dv.pages('"3_Permanent"').where(p => p.modified >= d).length;
var count_note_3m_13 = (count_note_3m / 13).toFixed(1);

// —— Last 6 Month —-
var count_note_6m = dv.pages('"3_Permanent"').where(p => p.modified >= e).length;
var count_note_6m_26 = (count_note_6m / 26).toFixed(1);

// —— Last 1 Year —-
var count_note_1Y = dv.pages('"3_Permanent"').where(p => p.modified >= f).length;
var count_note_1Y_52 = (count_note_1Y / 52).toFixed(1);

// —— Last 2 Years —-
var count_note_2Y = dv.pages('"3_Permanent"').where(p => p.modified >= g).length;
var count_note_2Y_104 = (count_note_2Y / 104).toFixed(1);

// —- All Since Start
var count_note_all = dv.pages('"3_Permanent"').length;
var note_per_week = (count_note_all / age_weeks).toFixed(1);

// --- show results ---
dv.paragraph('###### Modified per week till ' + a);

// --- Set Colors ---
const CHART_COLORS = {
	red: '#B51A00',
	orange: 'rgb(255, 159, 64)',
	yellow: '#FAC141',
	green: 'rgb(75, 192, 192)',
	blue: '#417CFA',
	black: '#000000',
	grey: '#CCCCCC',
	light_grey: '#DDDDDD',
	ultralight_grey: '#EEEEEE',
	dark_grey: '#AAAAAA',
	white: '#FFFFFF'
}

// --- Create Chart ---
const chartData = {
	type: 'bar',
	data: {
		labels: ['1W', '1M', '3M', '6M', '1Y', '2Y', 'ALL'],
		datasets: [
			{
			label: 'y',
			data: [count_note_1w, count_note_1m_13, count_note_3m_13,
					count_note_6m_26, count_note_1Y_52,
					count_note_2Y_104, note_per_week],
			backgroundColor: [
				CHART_COLORS.yellow,
				CHART_COLORS.ultralight_grey, CHART_COLORS.light_grey,
				CHART_COLORS.grey, CHART_COLORS.dark_grey, CHART_COLORS.black],
			borderColor: CHART_COLORS.white,
			borderWidth: 1
			}
		]
	},
	options: {
		indexAxis: 'x',
		plugins: {
			title: { display: false, text: 'Custom Chart Title' },
			subtitle: { display: false, text: 'Custom Chart Subtitle' },
			legend: { display: false, position: 'right' }
		}
	}
}

window.renderChart(chartData, this.container)

```

###### Notes Modified
```dataview
LIST
lead + " " + file.mday + "."
FROM "3_Permanent"
WHERE file.mday >= date(today) - dur(7 day)
SORT file.mday DESC
```

---
# Back Matter
## References
<!-- Links to pages not referenced in the content -->
- Built with the Obsidian Charts plugin

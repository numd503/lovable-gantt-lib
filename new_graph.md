---
title: Project Timeline NEW
hide:
  - navigation
  - toc
---

<div class="gantt-page">
# Project Timeline

<link rel="stylesheet" href="../assets/gantt-library.css">

<!-- Controls (file upload, releases toggle, filters) -->
<div id="gantt-controls"></div>

<!-- Filters panel (hidden by default) -->
<div id="gantt-filters-container" style="display: none;"></div>

<!-- Timeline container -->
<div class="gantt-timeline-wrapper">
<div id="timeline" style="width: 100%;"></div>
</div>
<!-- Legend -->
<div id="gantt-legend"></div>



<script src="../assets/gantt-library.js"></script>
<script>
  // Initialize GanttLibrary
  const gantt = new window.GanttLibrary({
    container: document.getElementById('timeline'),
    maxTaskNameLength: 40,
    colors: {
      analytics: '#6366f1',
      development: '#8b5cf6', 
      testing: '#10b981',
      release: '#f59e0b'
    },
    defaultView: 'month',
    labelWidth: '10%'
  });
  
  // Render UI controls (file upload, releases toggle, filter button)
  gantt.renderControls(document.getElementById('gantt-controls'));
  
  // Render legend
  gantt.renderLegend(document.getElementById('gantt-legend'));
  
  // Optional: Load data automatically on page load
  gantt.loadFromExcel('../data/plan_example.xlsx');

  // Optional: Load release dates automatically on page load
  gantt.loadReleasesFromExcel('../data/release_dates_example.xlsx');
</script>

</div>
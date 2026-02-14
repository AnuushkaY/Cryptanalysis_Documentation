---
title: Interactive Examples
nav_order: 5
layout: default
---

# Interactive Examples

This page demonstrates the interactive components embedded throughout the documentation.

## Mermaid Diagram

The following flowchart is rendered client‑side with **Mermaid.js**:

```mermaid
flowchart TD
    Input[Ciphertext] --> Model[Neural Network]
    Model --> Output[Prediction]
```

<script src="https://cdnjs.cloudflare.com/ajax/libs/mermaid/10.4.0/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>

## Chart.js Graph

Below is an interactive chart powered by **Chart.js** (loaded from CDN):

<canvas id="exampleChart" width="600" height="400"></canvas>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
const ctx = document.getElementById('exampleChart');
new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['AES','DES','Vigenère','Speck32'],
        datasets: [{
            label: 'Dummy Accuracy',
            data: [88,72,65,81],
            backgroundColor: 'rgba(54, 162, 235, 0.6)'
        }]
    },
    options: { responsive: true }
});
</script>
---
title: Results
nav_order: 4
layout: default
---

# Results

## Accuracy Table

| Cipher   | Accuracy |
|----------|----------|
| AES      | —        |
| DES      | —        |
| Vigenère | —        |
| Speck32  | —        |

## Key Rank Graph

<canvas id="keyRankChart" width="600" height="400"></canvas>

## Confusion Matrix

<canvas id="confusionChart" width="600" height="400"></canvas>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
// sample data - replace with real results
const keyRankCtx = document.getElementById('keyRankChart');
new Chart(keyRankCtx, {
  type: 'line',
  data: {
    labels: ['1','2','3','4','5','6','7','8','9','10'],
    datasets: [{
      label: 'Key Rank',
      data: [10,9,8,5,3,2,1,1,1,1],
      borderColor: 'rgb(75, 192, 192)',
      tension: 0.1
    }]
  },
  options: {
    responsive: true,
    plugins: {
      title: {
        display: true,
        text: 'Interactive Key Rank Curve'
      }
    }
  }
});

const confusionCtx = document.getElementById('confusionChart');
new Chart(confusionCtx, {
  type: 'bar',
  data: {
    labels: ['AES','DES','Vigenère','Speck32'],
    datasets: [
      {
        label: 'Correct',
        data: [90, 70, 60, 80],
        backgroundColor: 'rgba(75, 192, 192, 0.6)'
      },
      {
        label: 'Incorrect',
        data: [10, 30, 40, 20],
        backgroundColor: 'rgba(255, 99, 132, 0.6)'
      }
    ]
  },
  options: {
    responsive: true,
    plugins: {
      title: {
        display: true,
        text: 'Confusion Matrix (Correct vs Incorrect)'
      }
    },
    scales: {
      x: { stacked: true },
      y: { stacked: true }
    }
  }
});
</script>

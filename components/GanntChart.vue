<template>
  <div id="main" class="wrapper style3">
    <div class="container">
      <header class="major">
        <a name="Programme"></a><br /><br /><br />
        <h2>Work Programme</h2>
      </header>
      <div class="chart-wrapper" style="overflow-y: auto">
        <ul class="chart-values">
          <li>Jan 2021</li>
          <!-- <li>Feb 2021</li> -->
          <li>Mar 2021</li>
          <!-- <li>Apr 2021</li> -->
          <li>May 2021</li>
          <!-- <li>Jun 2021</li> -->
          <li>July 2021</li>
          <!-- <li>Aug 2021</li> -->
          <li>Sep 2021</li>
          <!-- <li>Oct 2021</li> -->
          <li>Nov 2021</li>
          <!-- <li>Dec 2021</li> -->
          <li>Jan 2022</li>
          <!-- <li>Feb 2022</li> -->
          <li>Mar 2022</li>
          <!-- <li>Apr 2022</li> -->
          <li>May 2022</li>
          <!-- <li>Jun 2022</li> -->
          <li>Jun 2022</li>
        </ul>
        <ul class="chart-bars">
          <li data-duration="Jan 2021-Jun 2022" data-color="#b03532">
            WP1000: Management and Reporting
          </li>
          <li data-duration="Jan 2021-Mar 2021" data-color="#33a8a5">
            WP2000: Consolidation of the scientific requirements
          </li>
          <li data-duration="Mar 2021-July 2021" data-color="#30997a">
            WP3000: Performance of regional short-term dust forecasts
          </li>
          <li data-duration="July 2021-Sep 2021" data-color="#6a478f">
            WP4000: Pre-processing and curation of the reference datasets
          </li>
          <li data-duration="Sep 2021-May 2022" data-color="#da6f2b">
            WP5000: Assessment of Aeolus profiles assimilation on dust
            monitoring and forecasting
          </li>
          <li data-duration="May 2022-Jun 2022" data-color="#3d8bb1">
            WP6000: Recommendations and future prespectives
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>


function  createChart(e) {
  console.log("CreateChart()!")

  const days = document.querySelectorAll(".chart-values li");
  const tasks = document.querySelectorAll(".chart-bars li");
  const daysArray = [...days];

  tasks.forEach((el) => {
    const duration = el.dataset.duration.split("-");
    const startDay = duration[0];
    const endDay = duration[1];
    let left = 0,
      width = 0;

    if (startDay.endsWith("½")) {
      const filteredArray = daysArray.filter(
        (day) => day.textContent == startDay.slice(0, -1)
      );
      left = filteredArray[0].offsetLeft + filteredArray[0].offsetWidth / 2;
    } else {
      const filteredArray = daysArray.filter(
        (day) => day.textContent == startDay
      );
      left = filteredArray[0].offsetLeft;
    }

    if (endDay.endsWith("½")) {
      const filteredArray = daysArray.filter(
        (day) => day.textContent == endDay.slice(0, -1)
      );
      width =
        filteredArray[0].offsetLeft +
        filteredArray[0].offsetWidth / 2 -
        left;
    } else {
      const filteredArray = daysArray.filter(
        (day) => day.textContent == endDay
      );
      width =
        filteredArray[0].offsetLeft + filteredArray[0].offsetWidth - left;
    }

    // apply css
    el.style.left = `${left}px`;
    el.style.width = `${width}px`;
    if (e.type == "load") {
      el.style.backgroundColor = el.dataset.color;
      el.style.opacity = 1;
    }
  });
}

export default {

mounted() {
window.addEventListener("load", createChart);
window.addEventListener("resize", createChart);
}

};
</script>

<style>
/* ----------------------GANT CHART CSS------------------------------------- */

/* RESET RULES
–––––––––––––––––––––––––––––––––––––––––––––––––– */
:root {
    --white: #fff;
    --divider: #ffffff;
    --body: #f5f7f8;
  }
  
  * {
    padding: 0;
	  margin: 0;
    box-sizing: border-box;
  }
  
  ul {
    list-style: none;
  }
  
  li {
	  list-style: none;
  }

  a {
    text-decoration: none;
    color: inherit;
  }
  
  body {
    background: var(--body);
    font-size: 16px;
    font-family: sans-serif;
    padding-top: 40px;
  }
  
  .chart-wrapper {
    max-width: 1250px;
    padding: 0 50px;
	/* margin: 0 auto; */
	align-content: inherit;
  }
  
  
  /* CHART-VALUES
  –––––––––––––––––––––––––––––––––––––––––––––––––– */
  .chart-wrapper .chart-values {
    position: relative;
    display: flex;
    margin-bottom: 20px;
    font-weight: bold;
    font-size: 1.2rem;
  }
  
  .chart-wrapper .chart-values li {
    flex: 1;
    min-width: 80px;
    text-align: center;
  }
  
  .chart-wrapper .chart-values li:not(:last-child) {
    position: relative;
  }
  
  .chart-wrapper .chart-values li:not(:last-child)::before {
    content: '';
    position: absolute;
    right: 0;
    height: 510px;
    border-right: 1px solid var(--divider);
  }
  
  
  /* CHART-BARS
  –––––––––––––––––––––––––––––––––––––––––––––––––– */
  .chart-wrapper .chart-bars li {
    position: relative;
    color: var(--white);
    margin-bottom: 15px;
    font-size: 16px;
    border-radius: 20px;
    padding: 10px 20px;
    width: 0;
    opacity: 0;
    transition: all 0.65s linear 0.2s;
  }
  
  @media screen and (max-width: 600px) {
    .chart-wrapper .chart-bars li {
      padding: 10px;
    }
  }

/* ------------------------ END OF GANTT CHART CSS --------------------------------------- */
</style>

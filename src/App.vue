<template>
  <main class="margin">
    <div class="table-container">
      <table class="">
        <thead>
          <tr>
            <th class="sticky-project-name sticky">Project Name</th>
            <th>Developer</th>
            <th>Main Contractor</th>
            <th>Address</th>
            <th>State</th>
            <th>Status</th>
            <th>Sector</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="project in data" :key="project.id" class="text-4D5964">
            <td
              class="cell sticky-project-name"
              :style="{ background: colors[project.id % colors.length] }"
            >
              {{ project.project_name }}
            </td>
            <td :style="{ background: colors[project.id % colors.length] }">
              {{ project.developer }}
            </td>
            <td :style="{ background: colors[project.id % colors.length] }">
              {{ project.main_contractor }}
            </td>
            <td :style="{ background: colors[project.id % colors.length] }">
              {{ project.address }}
            </td>
            <td :style="{ background: colors[project.id % colors.length] }">
              {{ project.state }}
            </td>
            <td
              class="text-C39B57"
              :style="{ background: colors[project.id % colors.length] }"
            >
              <span class="bg-FEE2B2"> {{ project.status }}</span>
            </td>
            <td :style="{ background: colors[project.id % colors.length] }">
              {{ project.sector }}
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </main>
</template>

<script setup>
import { ref } from "vue";
// import axios from "axios";
const data = ref([
  {
    id: 1,
    project_name: "Wuckert, Blanda and Crooks",
    developer: "Kerluke, Howe and Hammes PLC",
    main_contractor: "Gleason Group and Sons",
    address: "16 Mohr Street 36215 AdamVille",
    state: "Wyoming",
    status: "On hold",
    sector: "Institutional/Public Sector",
  },
  {
    id: 2,
    project_name: "Baumbach, Toy and Littel",
    developer: "Jacobs, Wiegand and Lind LLC",
    main_contractor: "Murray-Sanford LLC",
    address: "71 Dicki Street 00948 BettyeVille",
    state: "Hawaii",
    status: "On hold",
    sector: "Institutional/Public Sector",
  },
  {
    id: 3,
    project_name: "Wuckert, Blanda and Crooks",
    developer: "Kerluke, Howe and Hammes PLC",
    main_contractor: "Gleason Group and Sons",
    address: "16 Mohr Street 36215 AdamVille",
    state: "Wyoming",
    status: "On hold",
    sector: "Institutional/Public Sector",
  },
  {
    id: 4,
    project_name: "Baumbach, Toy and Littel",
    developer: "Jacobs, Wiegand and Lind LLC",
    main_contractor: "Murray-Sanford LLC",
    address: "71 Dicki Street 00948 BettyeVille",
    state: "Hawaii",
    status: "On hold",
    sector: "Institutional/Public Sector",
  },
  {
    id: 5,
    project_name: "Wuckert, Blanda and Crooks",
    developer: "Kerluke, Howe and Hammes PLC",
    main_contractor: "Gleason Group and Sons",
    address: "16 Mohr Street 36215 AdamVille",
    state: "Wyoming",
    status: "On hold",
    sector: "Institutional/Public Sector",
  },
  {
    id: 6,
    project_name: "Baumbach, Toy and Littel",
    developer: "Jacobs, Wiegand and Lind LLC",
    main_contractor: "Murray-Sanford LLC",
    address: "71 Dicki Street 00948 BettyeVille",
    state: "Hawaii",
    status: "On hold",
    sector: "Institutional/Public Sector",
  },
  {
    id: 7,
    project_name: "Wuckert, Blanda and Crooks",
    developer: "Kerluke, Howe and Hammes PLC",
    main_contractor: "Gleason Group and Sons",
    address: "16 Mohr Street 36215 AdamVille",
    state: "Wyoming",
    status: "On hold",
    sector: "Institutional/Public Sector",
  },
  {
    id: 8,
    project_name: "Baumbach, Toy and Littel",
    developer: "Jacobs, Wiegand and Lind LLC",
    main_contractor: "Murray-Sanford LLC",
    address: "71 Dicki Street 00948 BettyeVille",
    state: "Hawaii",
    status: "On hold",
    sector: "Institutional/Public Sector",
  },
]);
const colors = ["#FFF", "#F6FAFD"];

// const fetchData = async () => {
//   try {
//     const response = await axios.get("https://api.jsonserve.com/8wAB9P");
//     const jsonData = response.data;
//     data.value = jsonData.data; // Update the data with the fetched data
//   } catch (error) {
//     console.error("Error fetching data:", error);
//   }
// };

// onMounted(() => {
//   fetchData();
// });
</script>

<style scoped>
/* Basic CSS styles */
body {
  font-family: sans-serif;
}
.sticky {
  box-shadow: 5px 10px;
}
.margin {
  margin: 32px 8px;
}
.table-container {
  overflow-x: auto;
  border-radius: 10px;
  font-family: "Roboto", sans-serif;
}

table {
  width: 100%;
  border-collapse: collapse;
}

thead {
  color: white;
  text-align: left;
  text-transform: capitalize;
  font-size: 1rem;
  font-weight: bold;
}

th {
  padding: 28px 12px;
  font-weight: bold;
  background-color: #28394b;
}

tbody {
  width: 100%;
}

tr {
  font-weight: 400;
}

tr:nth-child(odd) {
  background-color: #fff;
}

tr:nth-child(even) {
  background-color: #f6fafd;
}

td {
  text-align: left;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  width: 100px;
  padding: 28px 12px;
}

@media screen and (min-width: 768px) {
  .sticky-project-name {
    position: sticky;
    left: 0;
    font-weight: bold;
  }
}

.text-4D5964 {
  color: #4d5964;
}

.text-C39B57 {
  color: #c39b57;
}

.bg-FEE2B2 {
  background-color: #fee2b2;
  padding: 2px 8px;
}
.cell {
  box-shadow: 5px 10px rgba(0, 0, 0, 0.2); /* Add box shadow to sticky-project-name */
  z-index: 2;
}
</style>

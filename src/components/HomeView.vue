<template>
  <div class="container">
    <h1>Full-stack Technical Examination</h1>

    <p class="subtitle">
      Complete all of the tasks below. All API endpoints should be consumed from the backend.
    </p>

    <!-- Connection Status -->
    <div class="card">
      <h2>Backend Connection</h2>

      <button
        class="status-btn"
        :class="connected ? 'connected' : 'disconnected'"
        @click="checkConnection"
      >
        Connect
      </button>

      <p class="description">
        Verify that the frontend can successfully connect to the backend API.
      </p>
    </div>

    <!-- Tasks -->
    <div class="card">
      <h2>Tasks</h2>

      <ol class="task-list">
        <li>
          Connect this frontend to the backend API.
          <ul>
            <li>
              Clicking the <strong>Connect</strong> button should call the API.
            </li>
            <li>
              If the connection succeeds:
              <ul>
                <li>Button color changes from blue to green.</li>
                <li>Button text changes from <strong>Connect</strong> to
                  <strong>Connected</strong>.
                </li>
              </ul>
            </li>
          </ul>
        </li>

        <li>
          Create a <strong>Normalization</strong> page.
          <ul>
            <li>Display the two normalized outputs using tables.</li>
            <li>Retrieve all data from the backend API.</li>
            <li>Convert the normalize sql query to eloquent.</li>
            <li>No hard-coded data is allowed.</li>
          </ul>

          <router-link class="page-link" to="/normalization">
            Open Normalization Page →
          </router-link>
        </li>

        <li>
          Create a complete CRUD module for Orders.
          <ul>
            <li>Create Order</li>
            <li>Edit Order</li>
            <li>Delete Order</li>
            <li>Display all orders in a table.</li>
            <li>Changes must immediately reflect in the frontend.</li>
            <li>All operations must use backend APIs.</li>
            <li>Validate all data</li>
            <li>Avoid duplication of inserting data</li>
          </ul>

          <router-link class="page-link" to="/orders">
            Open Orders CRUD →
          </router-link>
        </li>

        <li>
          Responsive UI (Frontend)
          <ul>
            <li>
              The application must be fully responsive.
            </li>
            <li>
              Support the following screen sizes:
              <ul>
                <li>Mobile (≤576px)</li>
                <li>Tablet (577–991px)</li>
                <li>Desktop (≥992px)</li>
              </ul>
            </li>
            <li>Tables should remain usable on smaller screens (e.g., horizontal scrolling or responsive layout).</li>
            <li>Buttons and forms should adjust appropriately without overlapping.</li>
          </ul>
        </li>
      </ol>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import axios from "../axios";

const connected = ref(false)

const checkConnection = async () => {
  /**
   * Replace with your API call.
   *
   * Example:
   *
   */

  // connected.value = true
   const response = await axios.get("test");

   let status = response.data.status

    if(status){
        connected.value = true;
    } else {
      connected.value = false;
    }

    console.log(response);
}


</script>

<template>
  <div class="container">
    <h1>Full-stack Technical Examination</h1>

    <p class="subtitle">
      Complete all of the tasks below. All API endpoints should be consumed from the backend.
    </p>

   <div class="card">
      <h2>Technical Examination Tasks</h2>

      <p class="description">
        Build a responsive Order Management System using Vue.js and the provided
        Laravel API. All data must come from the backend. Hard-coded data is not
        allowed unless specifically stated.
      </p>

      <ol class="task-list">

        <li>
          <strong>Backend Connection (10%)</strong>

          <ul>
            <li>Connect this frontend to the backend API.</li>
            <li>Clicking the <strong>Connect</strong> button should call the API.</li>
            <li>Use environment variables <strong>(.env)</strong> to configure and connect to the backend API. Hard-coded API URLs are not allowed.</li>
            <li>If the API responds successfully:
              <ul>
                <li>Button changes from blue to green.</li>
                <li>Text changes from <strong>Connect</strong> to <strong>Connected</strong>.</li>
              </ul>
            </li>
            <li>Display a user-friendly error message when the API is unavailable.</li>
          </ul>
        </li>

        <li>
          <strong>Normalization (10%)</strong>

          <ul>
            <li>Create a Normalization page.</li>
            <li>Display both normalized outputs using responsive tables.</li>
            <li>Retrieve data from the backend API.</li>
            <li>Convert the SQL normalization query into Laravel Eloquent.</li>
            <li>No hard-coded data.</li>
          </ul>

          <router-link class="page-link" to="/normalization">
            Open Normalization →
          </router-link>

        </li>

        <li>
          <strong>Order Management (30%)</strong>

          <ul>
            <li>Create Order</li>
            <li>Edit Order</li>
            <li>Delete Order</li>
            <li>View Order Details</li>
            <li>Display all orders using a responsive table.</li>
            <li>Use backend APIs only.</li>
            <li>Implement client-side validation.</li>
            <li>Prevent duplicate submissions.</li>
            <li>Show loading indicators.</li>
            <li>Display success and error notifications.</li>
            <li>Confirm before deleting.</li>
          </ul>

          <router-link class="page-link" to="/orders">
            Open Orders →
          </router-link>

        </li>

        <li>
          <strong>Coupon Management (20%)</strong>

          <ul>
            <li>Create a separate Coupon page accessible through the navigation bar.</li>
            <li>Create, Edit, Delete and List Coupons.</li>
            <li>Coupon fields:
              <ul>
                <li>Coupon Code</li>
                <li>Description</li>
                <li>Discount Type (Percentage / Fixed)</li>
                <li>Discount Value</li>
                <li>Minimum Purchase</li>
                <li>Expiration Date</li>
                <li>Status</li>
              </ul>
            </li>

            <li>Coupons must be selectable while creating or editing an order.</li>

            <li>Discount and Total Amount must be computed in the frontend.</li>

            <li>Display a meaningful message when a coupon cannot be applied.</li>

          </ul>

          <router-link class="page-link" to="/coupons">
            Open Coupons →
          </router-link>

        </li>

        <li>
          <strong>Responsive Design (10%)</strong>

          <ul>
            <li>Desktop</li>
            <li>Tablet</li>
            <li>Mobile</li>
            <li>Responsive Navigation Bar</li>
            <li>Responsive Forms</li>
            <li>Responsive Tables</li>
            <li>No overlapping elements.</li>
          </ul>

        </li>

        <li>
          <strong>Analytical & Critical Thinking (15%)</strong>

          <p>The API intentionally does not provide every computed value.</p>

          <ul>
            <li>Compute Order Total.</li>
            <li>Compute Coupon Discount.</li>
            <li>Prevent discount from exceeding subtotal.</li>
            <li>Prevent expired coupons from being applied.</li>
            <li>Prevent inactive coupons from being used.</li>
            <li>Prevent orders below the coupon's minimum purchase.</li>
            <li>Gracefully handle null or missing API values.</li>
            <li>Display appropriate loading and error states.</li>
          </ul>

        </li>

        <li>
          <strong>Code Quality (5%)</strong>

          <ul>
            <li>Reusable Vue components.</li>
            <li>Clean folder structure.</li>
            <li>Meaningful variable names.</li>
            <li>Proper API separation.</li>
            <li>Readable and maintainable code.</li>
          </ul>

        </li>

        <li>
          <strong>Bonus (Optional)</strong>

          <ul>
            <li>Search Orders</li>
            <li>Pagination</li>
            <li>Sorting</li>
            <li>Dashboard Summary Cards</li>
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
   

   let status = "";

    if(status){
        connected.value = true;
    } else {
      connected.value = false;
    }

}


</script>

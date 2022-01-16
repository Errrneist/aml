---
title: CS 5787 - Applied Machine Learning
subtitle: Lorem ipsum dolor sit amet.
layout: page
show_sidebar: false
hero_height: is-medium
---
<div class="columns">
    <div class="column is-6">
        <h2>Lorem Ipsum</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
        <hr>
        <div class = "columns">
        <div class="column is-4">
            <center><button class="button is-primary is-outlined">About</button></center>
        </div>
        <div class="column is-4">
            <center><button class="button is-primary is-outlined">Prerequisites</button></center>
        </div>
        <div class="column is-4">
            <center><button class="button is-primary is-outlined">Affiliates</button></center>
        </div>
    </div>
    </div>
    <div class="column is-6">
        {% include youtube.html video="vcE9WGbi4QY" %}
    </div>
</div>



***

<div class="container">
    <h2>Chapter 1: Lorem ipsum.</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    <div class="columns">
        <div class="column is-4">
            <h3>Videos</h3>
            <div class="dropdown">
                <div class="dropdown-trigger">
                    <button class="button is-primary is-light" aria-haspopup="true" aria-controls="dropdown-menu">
                      <span>Video Button</span>
                      <span class="icon is-small">
                        <i class="fas fa-angle-down" aria-hidden="true"></i>
                      </span>
                    </button>
                </div>
                <div class="dropdown-menu" id="dropdown-menu" role="menu">
                    <div class="dropdown-content">
                      <a href="https://www.cornell.edu" class="dropdown-item">
                        Cornell
                      </a>
                      <a href="https://www.google.com" class="dropdown-item">
                        Google
                      </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="column is-4">
            <h3>Lecture Notes</h3>
            <button class="button is-link is-light">Note 1</button>
            <button class="button is-link is-light">Note 2</button>
        </div>
        <div class="column is-4">
            <h3>Additional Material</h3>
            <button class="button is-info is-light">Extra Reading 1</button>
            <button class="button is-info is-light">Extra Reading 2</button>
        </div>
    </div>
</div>

<script>
// Script for making dropdown functional.
// Reference: https://stackoverflow.com/a/58405701
// Get all dropdowns on the page that aren't hoverable.
const dropdowns = document.querySelectorAll('.dropdown:not(.is-hoverable)');

if (dropdowns.length > 0) {
  // For each dropdown, add event handler to open on click.
  dropdowns.forEach(function(el) {
    el.addEventListener('click', function(e) {
      e.stopPropagation();
      el.classList.toggle('is-active');
    });
  });

  // If user clicks outside dropdown, close it.
  document.addEventListener('click', function(e) {
    closeDropdowns();
  });
}

/*
 * Close dropdowns by removing `is-active` class.
 */
function closeDropdowns() {
  dropdowns.forEach(function(el) {
    el.classList.remove('is-active');
  });
}

// Close dropdowns if ESC pressed
document.addEventListener('keydown', function (event) {
  let e = event || window.event;
  if (e.key === 'Esc' || e.key === 'Escape') {
    closeDropdowns();
  }
});
</script>

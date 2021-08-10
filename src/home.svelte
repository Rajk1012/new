
<script lang="ts">
    import '@shoelace-style/shoelace/dist/themes/base.css'
  import 'medblocks-ui'
  import './tailwind.css'
  import axios from  "axios"
 
  import { Router, Link, Route } from "svelte-routing"
  import home from './home.svelte'  
  </script>

<div>
        <div class="container">
        <Link to="/form" class="link">New Patient</Link>
        </div>
        <div class="container">
        <Link to="/Patient" class="link">Get Patient Info</Link>
        </div>
        <div class="container">
        <Link to="/post" class="link">Post Covid Care</Link>
        </div>
</div>
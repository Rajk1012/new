<script lang="ts">
    import '@shoelace-style/shoelace/dist/themes/base.css'
  import 'medblocks-ui'
  import './tailwind.css'
  import axios from  "axios"
  import form from './form.svelte'
  import { Router, Link, Route } from "svelte-routing"
  import home from './home.svelte'  
  </script>

<div>
    <div>
        <Link to="/form" class="link">New Patient</Link>
        </div>
      
        <div>
        <Link to="/info" class="link">Get Patient Info</Link>
        </div>
        <div>
        <Link to="/post" class="link">Post Covid Care</Link>
        </div>
</div>
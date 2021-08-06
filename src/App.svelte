<script lang="ts">
  import '@shoelace-style/shoelace/dist/themes/base.css'
import 'medblocks-ui'
import './tailwind.css'
import axios from  "axios"
import form from './form.svelte'
import { Router, Link, Route } from "svelte-routing"
import home from './home.svelte'
import List from './List.svelte'
// import {Buttons} from "svelte-bootstrap"

</script>
<style>
	@import url("https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css");
</style>

<div class="container mt-5">
  <Router>
    <nav>
      <ul>
          <Link to="/">Home</Link>
          <Link to="/form">Registration Form</Link>
          <Link to="/Patient">Patients</Link>
        
      </ul>
    </nav>
      <!-- <Route path="/Patient" component={post}></Route> -->
    <Route path="/" component={home}></Route>
    <Route path="/Patient" component={List}/>
    <Route path="/form" component={form}/>
  </Router>
</div>






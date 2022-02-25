<script>
    import supabase from '$lib/db';

    async function logout() {
   	 const { error } = await supabase.auth.signOut();

   	 if (error) alert(error.message); // alert if error
    }

</script>
<h1>My Dashboard</h1>
<table class="table table-dark table-striped text-center caption-top">
    <caption>School Timetable</caption>
    <thead>
      <tr>
        <th scope="col">DAY</th>
        <th scope="col">1</th>
        <th scope="col">2</th>
        <th scope="col">3</th>
        <th scope="col">4</th>
        <th scope="col">-</th>
        <th scope="col">5</th>
        <th scope="col">6</th>
        <th scope="col">7</th>
        <th scope="col">8</th>
        <th scope="col">9</th>
        <th scope="col">10</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row">MON</th>

      </tr>
      <tr>
        <th scope="row">TUE</th>

      </tr>
      <tr>
        <th scope="row">WED</th>
      </tr>
      <tr>
        <th scope="row">THU</th>

      </tr>
      <tr>
        <th scope="row">FRI</th>

      </tr>
    </tbody>
  </table>

<!-- Sign Out -->
<section class="container px-4 py-3 text-center">
    <button class="btn btn-secondary" on:click={logout}>Logout</button>
</section>	